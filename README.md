# Emotion Restaurant Recommend System
감정 인식 기반 맛집 추천 시스템

# 소개
Emotion Restaurant Recommend System(ERS)는
**KoBERT 모델**과 **CBF NCF 알고리즘**을 활용하여, 감정 텍스트 인식을 기반으로, CBF와 NCF로 각 감정에 맞는 위치 기반 맛집을 추천하는 서비스입니다.
이 프로젝트는 20년도때 학교에 코로나로 학교에 오지 못해 슬펐던 기억과, 그로인해 주변의 맛집을 모르는 경우 있어 이경우에 어디에 가야되지? 하는 생각으로 프로젝트를 진행하게 되었씁니다.

# 주요 기능
텍스트로 감정 인식을 하여 해당 감정에 맞는 음식과 해당 음식 카테고리에 맞는 맛집을 실시간 위치 기반으로 맛집 추천

1. KoBERT로 감정 데이터를 수집하여, 텍스트를 분석하여 해당 텍스트의 감정을 인식합니다.
2. 추출된 감정을 통하여, 감정에 따른 감정 완화 음식을 추천합니다 (CBF)
3. 음식에 따른 카카오API를 활용하여, 위치에 따른 맛집을 추천합니다. (NCF)
4. GPS 데이터를 수집하여 군중의 위치와 이동 패턴을 실시간으로 분석합니다.

검색 창처럼, 자신의 감정을 입력합니다.
감정을 기반으로 감정 안화를 위한 음식을 추천하며 자동적으로
해당 음식에 관한 맛집을 자신의 위치를 기반으로 추천합니다.
사용자 인터페이스(UI/UX)


프로젝트 구조
프론트엔드

모바일 애플리케이션: Android Studio 사용
백엔드

서버 프레임워크: Django 사용
통신 방식: RESTful API 및 WebSocket
머신러닝

모델 개발: TensorFlow 활용
기능: 군중 밀집도 예측 및 실시간 데이터 분석
데이터베이스

주 데이터베이스: PostgreSQL
캐시 및 세션 관리: Redis
DevOps

컨테이너화: Docker 사용
CI/CD: Jenkins 및 GitLab CI/CD
클라우드 인프라: AWS 활용
설치 및 실행 방법
전제 조건
Python 3.8 이상
Docker 및 Docker Compose
AWS 계정 (또는 다른 클라우드 서비스)
백엔드 설정
저장소 클론

git clone https://github.com/yourusername/safecrowd.git
cd safecrowd/backend
가상환경 생성 및 활성화

python -m venv venv
source venv/bin/activate  # Windows의 경우 'venv\Scripts\activate'
종속성 설치

pip install -r requirements.txt
환경 변수 설정

.env 파일을 생성하고 필요한 환경 변수를 설정합니다.
데이터베이스 마이그레이션

alembic upgrade head
서버 실행

python3 manage.py runserver
프론트엔드 설정
저장소 클론 (이미 클론한 경우 생략)

cd ../frontend
종속성 설치

npm install
환경 변수 설정

.env 파일을 생성하고 필요한 환경 변수를 설정합니다.
애플리케이션 실행

npm start
Docker를 이용한 전체 서비스 실행
루트 디렉토리에서 Docker Compose 실행

docker-compose up --build
사용 방법
앱 접속

모바일 앱 또는 웹 애플리케이션에 접속합니다.
초기 설정

위치 정보 제공 및 알림 수신에 동의합니다.
홈 화면

현재 위치와 주변의 군중 밀집도를 확인합니다.
경로 안내

목적지를 설정하면 안전한 경로 안내를 받습니다.
재난 알림 수신

재난 상황 발생 시 실시간 경고 알림을 수신하고 대피 경로를 제공합니다.
제보 및 공유

위험 요소나 재난 상황을 제보하여 다른 사용자들과 정보를 공유합니다.
기여 방법
저장소 포크

이 저장소를 포크합니다.
브랜치 생성

새로운 기능이나 버그 수정을 위한 브랜치를 생성합니다.
변경 사항 커밋

기능을 추가하거나 버그를 수정한 후 커밋합니다.
푸시 및 Pull Request 생성

변경 사항을 푸시하고 Pull Request를 생성합니다.
리뷰 및 병합

리뷰 후 프로젝트에 병합됩니다.
라이선스
이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 LICENSE 파일을 참조하세요.

팀 구성
프로젝트 매니저 및 백엔드 개발자

이름: 한동혁
역할: 프로젝트 관리, 백엔드 개발, API 개발
백엔드 개발자 및 서버 아키텍트

이름: 진건호
역할: 백엔드 개발, 서버 구축, API 개발
머신러닝 엔지니어 및 데이터 사이언티스트

이름: 김지훈
역할: 데이터 수집 및 분석, 머신러닝 모델 개발
QA 엔지니어 및 DevOps 전문가

이름: 박민호
역할: 품질 보증, CI/CD 파이프라인 구축, 시스템 모니터링
프론트 엔드 및 UI/UX 개발

이름: 김동건
역할: 프론트 엔드 개발, UI/UX 개발
연락처
이메일: donghyeok7312@naver.com
이슈 트래커: GitHub Issues
참고 자료
TensorFlow 공식 문서: https://www.tensorflow.org/
FastAPI 공식 문서: https://fastapi.tiangolo.com/
Docker 공식 문서: https://docs.docker.com/
