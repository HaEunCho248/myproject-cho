## 프론트엔드 배포 파이프라인
![프론트엔드 배포 파이브라인 이미지](./images/frontend-deployment-pipeline.png)

진행 순서 
  1. 저장소를 체크아웃 한다.
  2. 프로젝트 의존성을 설치한다.
  3. Next.js 프로젝트를 빌드한다.
  4. AWS 자격 증명을 구성한다.
  5. 빌드된 파일을 S3 버킷에 동기화한다.
  6. CloudFront 캐시를 무효화한다.

## 주요 링크
- S3 버킷 웹사이트 엔드포인트 : http://rjadmszhd7777-aws-bucket.s3-website.eu-north-1.amazonaws.com
- CloudFrount 배포 도메인 이름 : https://d1vdf9tjtc0bf5.cloudfront.net

## 주요개념
- GitHub Actions과 CI/CD 도구 : Github의 워크플로우 자동화 도구로, 코드 변경 시 자동으로 빌드/테스트/배포를 수행
- S3와 스토리지 : AWS의 확장 가능한 객체 스토리지 서비스로, 정적 웹사이트 호스팅에 사용
- CloudFront와 CDN : AWS의 콘텐츠 전송 네트워크(CDN) 서비스로, 전세계 엣지 로케이션을 통해 콘텐츠를 빠르게 전달
- 캐시 무효화(Cache Invalidation) : CloudFront의 캐시된 콘텐츠를 강제로 업데이트하여 최신 버전을 제공하는 프로세스
- Repository secret과 환경변수 :GitHub에서 제공하는 보안 값 저장 기능으로, AWS 접근키 등 민감한 정보를 안전하게 관리
