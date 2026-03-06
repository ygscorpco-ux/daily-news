# Daily News Vercel 배포 가이드

## 구조
- 고객용: `customer/`
- 관리자용(로컬): `admin/`

`admin/`은 `.vercelignore`로 배포 제외됩니다.

## 1) 고객용 배포
1. Vercel에서 이 저장소를 연결합니다.
2. Root Directory는 기본(`.`) 그대로 두거나 `customer`로 지정해도 됩니다.
3. Production 배포를 실행합니다.
4. 카카오 채널 URL은 Vercel Production URL로 설정합니다.

## 2) 관리자 사용
1. 로컬에서 `admin/index.html`을 브라우저로 엽니다.
2. ZIP 업로드 -> TSV/정리 ZIP 생성.
3. 정리 ZIP을 풀어 `customer/images/`를 갱신합니다.
4. `news.tsv`를 Google Sheets에 붙여넣습니다.
5. 고객용만 다시 배포합니다.

## 참고
- 루트 `index.html`은 `customer/index.html`로 리다이렉트합니다.
- 고객에게는 관리자 URL을 공유하지 않습니다.
