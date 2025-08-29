# 🚀 Mini Data Engineering Project (Kafka + Spark + MySQL + Airflow)

이 프로젝트는 **데이터 엔지니어링 핵심 워크플로우(ETL 파이프라인)**를 직접 구현해보기 위한 학습/포트폴리오용 프로젝트입니다.  
Docker 기반으로 Kafka, MySQL, Airflow를 실행하고, 로컬 PySpark를 활용해 데이터를 처리합니다.

---

## 📂 프로젝트 개요

- **데이터 수집 (Extract)**  
  Kafka Producer(Python) → 토픽(weather)으로 메시지 발행  

- **데이터 변환 (Transform)**  
  PySpark Structured Streaming → JSON 메시지를 파싱 & 전처리  

- **데이터 저장 (Load)**  
  처리된 데이터를 MySQL에 적재  

- **워크플로우 자동화 (Orchestration)**  
  Airflow DAG → 매일 새벽 배치 집계 실행  

---

## 🛠 사용 기술 스택

- **Infra**: Docker, Docker Compose  
- **Messaging**: Apache Kafka, Zookeeper  
- **Database**: MySQL 8.0  
- **Processing**: PySpark (Structured Streaming)  
- **Orchestration**: Apache Airflow  
- **Language**: Python 3.x  
- **ETL Framework**: Pandas, SQLAlchemy, kafka-python  

---

## 📂 프로젝트 구조
```
de-mini-etl/
├── docker-compose.yml # Docker 환경 (Kafka, Zookeeper, MySQL, Airflow)
├── dags/ # Airflow DAGs
│ └── weather_etl.py
├── spark/ # Spark 처리 코드
│ └── spark_stream.py
├── producer/ # Kafka Producer 코드
│ └── producer.py
└── README.md
```

