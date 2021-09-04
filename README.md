# MSA-Dev-SpringCloud
Microservice Application with SpringCloud


1. [Service Discovery](https://www.notion.so/1-Service-Discovery-0ce760370a4745049a6cb7d533c08a41)
2. [API Gateway](https://www.notion.so/2-API-Gateway-Service-6067ff34af334b68b62bb31727513302)
3. [E-commerce 애플리케이션](https://www.notion.so/3-E-commerce-ef080a18f84442338e1e7fe2aa22d457)
4. [Users Microservice](https://www.notion.so/4-Users-Microservice-0b81b862fd8541cbb37a5a5d9ec48374)
5. 보류
6. [UserMicroservice (인증과 권한)](https://www.notion.so/6-UserMicroservice-a56d8c61c3c64cde83b800e6cd7a31ca)
7. [Configuration Service](https://www.notion.so/7-Configuration-Service-fbedb62c4e1f45beb6d10a8d8a8476a7)
8. [Spring Cloud Bus](https://www.notion.so/4-Users-Microservice-0b81b862fd8541cbb37a5a5d9ec48374)
9. [암호화 처리를 위한 encryption과 decryption](https://www.notion.so/9-encryption-decryption-114a825c3d7042eb8580ba2534f7776a)
10. [Microservice간 통신 ](https://www.notion.so/10-Microservice-d78b2cce4b8e45cb8bcc12331b422625)
11. [데이터 동기화를 위한 Kafka 활용 -1](https://www.notion.so/11-Kafka-1-65a2e138848f4cc2bdcca61306ca59f0)
12. [데이터 동기화를 위한 Apache Kafka의 활용 - 2](https://www.notion.so/12-Apache-Kafka-2-41891d89afb946e3828c795b3232fd91)
13. 보류
14. 보류
15. [애플리케이션 배포를 위한 컨테이너 가상화 (Docker)](https://www.notion.so/15-8b44db4f71c248f3a52f19f0a04083cf)




----------------

# 애플리케이션 배포를 위한 컨테이너 가상화 


## 가상화 (Virtualization)

- 물리적인 컴퓨터 리소스를 다른 시스템이나 애플리케이션에서 사용할 수 있도록 제공

### OS Virtualization

- Host OS위에 Guest OS 전체를 가상화
- VMWare, VirtualBox
- 자유도가 높으나, 시스템에 부하가 많고 느려짐

### Container Virtualization

- Host OS가 가진 리소스를 적게 사용하며, 필요한 프로세스 실행
- 최소한의 라이브러리와 도구만 포함
- Container의 생성 속도가 빠름

### Container Image

- Container 실행에 필요한 **설정 값**
    - 상태값 X, immutable
- Image를 가지고 실체화 → **Container**

    (Image만 가지고 있어도 하나의 소프트웨어 및 운영체제를 실행할 수 있다)

### Dockerfile

- Docker Image를 생성하기 위한 스크립트 파일
- 자체 DSL(Domain-Specific language) 언어 사용 → 이미지 생성과정 기술

## 설치

- Docker Desktop 설치

[Docker Desktop for Mac and Windows | Docker](https://www.docker.com/products/docker-desktop)

## 도커 명령어

- docker info: 설치 정보 확인
- docker image ls: 이미지 목록 확인
- docker container ls: 컨테이너 목록 확인
- docker run: 컨테이너 실행

    ```bash
    docker run [OPTIONS] IMAGE[:TAG|@DIGEST][COMMAND][ARG...]
    ```

    [Docker Run Options](https://www.notion.so/5a15209bfe764f0681d62d445f2ef621)

### Ubuntu Test

1. 설치: docker pull ubuntu:16.04
2. 실행: docker run ubuntu
3. 실행 이력 확인: docker container ps -a
4. 제거: docker rm b4ec3363963b
5. container 목록 확인: docker container ls -a
