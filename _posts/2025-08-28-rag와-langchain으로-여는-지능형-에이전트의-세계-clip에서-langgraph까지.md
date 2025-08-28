---
title: "RAG와 LangChain으로 여는 지능형 에이전트의 세계: CLIP에서 LangGraph까지"
date: 2025-08-28 17:09:32 +0900
categories: [기술]
tags: [Python, 머신러닝]
toc: true
comments: false
mermaid: true
math: true
---

# RAG와 LangChain으로 여는 지능형 에이전트의 세계: CLIP에서 LangGraph까지

현대 AI의 핵심은 저장된 지식과 실시간 검색을 결합하는 RAG입니다. CLIP 같은 임베딩 모델과 Vectorstore, Document Loader가 데이터를 준비하고, LM이 답을 만듭니다. 여기에 Memory, Tools, Agent, Chain이 더해져 대화형 지능이 작동합니다. LangChain은 이 파이프라인을 쉽게 엮고, LangGraph로 구성요소 간 연결성을 한층 강화합니다. 로컬 실행의 이점은 Ollama 같은 런타임으로 누릴 수 있으며, PART 같은 모듈형 설계로 확장도 수월합니다.

핵심 구성요소
- CLIP: 멀티모달 임베딩의 예시
- Embedding Model: 텍스트 임베딩의 핵심
- Vectorstore: 벡터를 저장하는 저장소
- Document Loader: 데이터를 수집하고 정렬
- Memory: 대화 맥락과 정보를 기억
- Tool/Agent: 외부 작업 수행 및 환경과의 상호작용
- Chain: 실행 흐름의 구성 단위
- LM: 실제 응답 생성
- Graph/LangGraph: 구성요소 간 그래프 연결
- Ollama: 로컬 LLM 런타임
- PART/RAG with LangChain: 구현과 운영 방식

작동 흐름
문서가 Document Loader로 들어와 Embedding Model(CLiP 등)로 벡터화됩니다. 벡터는 Vectorstore에 저장되고, 필요 시 Retrieval으로 LM이 관련 정보를 바탕으로 응답을 구성합니다. Memory가 맥락을 유지하고, Agent가 Tools를 활용해 외부 작업을 수행합니다. Chain은 각 단계의 순서를 제시하고, LangGraph는 전체 구성의 관계를 시각화하고 확장합니다. 로컬 환경에서 Ollama로 실행하면 지연을 줄이고 프라이버시를 강화할 수 있습니다.

결론
CLIP 기반 임베딩과 벡터저장소로 시작해, LangChain과 LangGraph로 구성요소를 연결하는 RAG 파이프라인이 현대 지능형 에이전트의 핵심입니다. 로컬 런타임과 모듈형 설계로 확장성과 재사용성을 높이며, 실무에서 데이터 인사이트와 자동화를 동시에 구현할 수 있습니다.