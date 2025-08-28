---
title: "CLIP과 LangChain으로 여는 RAG 기반 지식 검색의 세계"
date: 2025-08-28 17:14:11 +0900
categories: [기술]
tags: [Python]
toc: true
comments: false
mermaid: true
math: true
---

## CLIP과 LangChain으로 여는 RAG 기반 지식 검색의 세계

CLIP은 텍스트와 이미지를 같은 임베딩 공간에 매핑하는 멀티모달 모델로 시작합니다. 이 임베딩은 Embedding model로 만들어지고, Vectorstore에 저장되어 빠른 유사도 검색이 가능해집니다. 문서 원문은 Document loader로 시스템에 불러들이고, 필요하면 Recap으로 핵심을 요약합니다. 

RAG(Retrieval-Augmented Generation) 방식에서 LM은 검색된 문서를 바탕으로 더 정확한 답을 생성합니다. LangChain은 이 흐름을 Agent, Tool, Memory, Chain 같은 구성요소로 구성해 자동화합니다. 지식의 관계를 Graph 형태로 정리하는 Graph Recap도 활용 가능하며, 로컬 실행 대안으로 Ollama PART를 통해 로컬 LLM 운영도 고려할 수 있습니다.

구현 흐름은 간단합니다. Document loader → Embedding model → Vectorstore 저장 → Retrieval → LM이 문서 기반으로 응답 생성. Ollama PART로 로컬에서 실행하는 옵션은 프라이버시와 지연 시간을 줄여줍니다.

핵심 요약: CLIP으로 멀티모달 이해를 시작으로 벡터스토어와 RAG로 신뢰도 높은 답을 빠르게 얻고, LangChain의 Agent/Tool/Memory/Chain으로 워크플로우를 자동화합니다. Graph Recap으로 지식 망을 관리하고, Ollama PART로 로컬 실행 옵션을 확보합니다.