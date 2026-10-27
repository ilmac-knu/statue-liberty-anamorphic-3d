# ㉙ 자유의 여신상 — Anamorphic 3D 화면 밖 돌출 애니메이션

스마트폰 속 뉴욕 항구에서 자유의 여신상이 솟아오르고, 마지막에는 황금 횃불을 관람객 쪽으로 내미는 **자동 2.5D 원근 착시 애니메이션**입니다.

## 실행 주소

https://ilmac-knu.github.io/statue-liberty-anamorphic-3d/

## 저장소 파일 구조

```text
statue-liberty-anamorphic-3d/
├── index.html
├── README.md
├── liberty-background.png
├── liberty-statue-transparent.png
└── liberty-torch-transparent.png
```

**중요:** 원래 첨부한 `liberty-statue.png`, `liberty-torch.png`에는 회색 바둑판 배경이 실제 픽셀로 들어 있어 그대로 겹치면 사각형이 보입니다. 함께 제공한 `*-transparent.png` 파일을 사용하세요. 원본 두 장은 업로드하지 않아도 됩니다.

## 실행 순서

1. 위 5개 파일을 GitHub 저장소 최상위에 업로드합니다.
2. **Settings → Pages → Build and deployment → Deploy from a branch**를 선택합니다.
3. Branch는 `main`, 폴더는 `/ (root)`로 설정하고 저장합니다.
4. 배포가 완료되면 위 실행 주소에 접속합니다.
5. **▶ 돌출 애니메이션 시작**을 누릅니다. **↻ 다시 보기**, **⏸ 일시정지**도 사용할 수 있습니다.

## 연출 구성

| 구간 | 연출 |
|---|---|
| 0~3.7초 | 자유의 여신상이 화면 안에서 점차 확대 |
| 2.9~5.7초 | 화면 밖으로 솟아오르는 돌출감 강화 |
| 5.1~7.7초 | 별도 횃불·오른팔 이미지가 관람객 방향으로 확대·이동 |
| 8.5초 | 최종 화면 유지 |

## 기술 및 한계

- HTML5 Canvas, JavaScript, 투명 PNG 레이어, 확대/이동/그림자 기반 원근 착시
- 카메라·헤드셋·GLB 파일 불필요
- 실제 입체 디스플레이 또는 시점 추적형 3D가 아닌 **단일 시점용 2.5D 합성 애니메이션**
- 별도 제작한 횃불 레이어와 여신상 원본의 오른팔이 일부 겹쳐 보일 수 있습니다. 완벽한 관절 애니메이션에는 동일 원본에서 분리한 팔 이미지나 리깅된 3D 모델이 필요합니다.

## 사용 이미지

- `liberty-background.png`: 뉴욕 항구와 스마트폰
- `liberty-statue-transparent.png`: 여신상 상반신
- `liberty-torch-transparent.png`: 황금 횃불과 오른팔
