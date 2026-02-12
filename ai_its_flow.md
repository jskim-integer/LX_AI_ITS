graph TD
    %% 스타일 정의
    classDef step1 fill:#E3F2FD,stroke:#1565C0,stroke-width:2px;
    classDef step2 fill:#E8F5E9,stroke:#2E7D32,stroke-width:2px;
    classDef step3 fill:#FFF3E0,stroke:#EF6C00,stroke-width:2px;
    classDef step4 fill:#F3E5F5,stroke:#7B1FA2,stroke-width:2px;
    classDef core fill:#FFEBEE,stroke:#D32F2F,stroke-width:4px;

    subgraph Phase1 [1. 민관 데이터 연계 및 통합 (Foundation)]
        A1[거버넌스 구축 및 운영<br/>(협의체, 공유 규칙)]
        A2[데이터 표준화<br/>(연계 규격, 분류 체계)]
        A3[실시간 통합 기술<br/>(공공/민간 API 연계)]
    end

    subgraph Phase2 [2. AI기반 데이터 가공/품질관리 (Processing)]
        B1[데이터 품질 관리<br/>(결측치/이상치 자동보정)]
        B2[데이터 구조화<br/>(메타정보 식별, 벡터DB)]
        B3[개인정보 보호<br/>(비식별화, 암호화)]
    end

    subgraph Phase3 [3. AI 고품질 정보 합성 및 예측 (AI Core)]
        C1[엣지케이스 생성 :::core<br/>(3D 합성, 증강 기술)]
        C2[LLM 기반 예측<br/>(교통정보 합성, 자연어 분석)]
        C3[위험 상황 예측<br/>(돌발, 재난, 사고 예측)]
    end

    subgraph Phase4 [4. 플랫폼 구축 및 실증 (Service & Verify)]
        D1[클라우드 플랫폼<br/>(Kubernetes, MLOps)]
        D2[AI 의사결정 지원<br/>(AI Agent, 대응 시나리오)]
        D3[실도로/시뮬레이션 실증<br/>(디지털트윈, 현장검증)]
    end

    %% 흐름 연결
    Phase1 --> Phase2
    Phase2 --> Phase3
    Phase3 --> Phase4
    
    %% 세부 흐름
    A3 --> B1
    B1 --> B2
    B2 --> C1
    C1 --> C2
    C2 --> C3
    C3 --> D2
    D1 -.-> D2
    D2 --> D3

    %% 클래스 적용
    class A1,A2,A3 step1;
    class B1,B2,B3 step2;
    class C1,C2,C3 step3;
    class D1,D2,D3 step4;
