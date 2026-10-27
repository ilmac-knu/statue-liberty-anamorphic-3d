# ㉙ 자유의 여신상 · Anamorphic 3D

스마트폰 화면에 표시된 뉴욕 항구에서 자유의 여신상이 솟아오르며 황금 횃불을 관람객 쪽으로 내미는 **2.5D 원근 착시 애니메이션**입니다. 스마트폰 카메라 화면 위에도 같은 콘텐츠를 합성할 수 있습니다.

## 파일 구성

- `index.html` — 애니메이션, 카메라 합성, 터치 조작 구현
- `liberty-background.png` — 자유의 여신상이 없는 스마트폰·뉴욕 항구 배경 (투명 PNG)
- `liberty-statue-transparent.png` — 자유의 여신상 상반신·횃불 이미지 (투명 PNG)

별도의 `liberty-torch.png`는 사용하지 않습니다.

## 사용 방법

1. 웹페이지 접속 후 **▶ 돌출 시작**을 누르면 자유의 여신상이 솟아오릅니다.
2. **↻ 다시 보기**로 처음부터 재생합니다.
3. **📷 카메라 켜기**를 누르고 카메라 권한을 허용하면 실제 책상·바닥 영상 위에 합성됩니다.
4. **📍 위치 배치**를 누른 후 화면을 터치해 위치를 지정합니다.
5. 한 손가락으로 전체를 이동하고, 두 손가락으로 확대·축소 및 평면 회전합니다. 버튼으로도 확대·축소할 수 있습니다.
6. **처음 위치**로 배치와 크기를 초기화합니다.

## GitHub Pages 배포

위 3개 파일을 저장소 `ilmac-knu/statue-liberty-anamorphic-3d` 루트에 업로드합니다. **Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save**를 선택합니다.

배포 주소: https://ilmac-knu.github.io/statue-liberty-anamorphic-3d/

## 기술과 한계

- HTML/CSS/JavaScript, PNG 이미지 2장, CSS 키프레임 애니메이션, `getUserMedia()` 카메라 합성, Pointer Events 터치 제스처를 사용합니다.
- **실제 GLB 3D 모델 또는 공간 추적 AR이 아닙니다.** 회전은 평면 이미지 회전이며 옆면을 볼 수 없습니다.
- 카메라 합성 이미지는 화면 좌표에 놓입니다. 현실 바닥의 특정 위치에 고정되는 월드 앵커는 제공하지 않습니다.
- 카메라 권한과 HTTPS 환경이 필요하며, 브라우저별 카메라 지원에 차이가 있습니다.
- 이미지의 크기와 위치는 `index.html`의 `.statue` CSS (`width`, `left`, `top`)를 수정해 미세 조정할 수 있습니다.
