# ₿ UP or DOWN — Bitcoin Prediction Game

15초 뒤 비트코인 가격이 오를지 내릴지 맞히는 심심풀이 웹게임.
Guess whether Bitcoin goes UP or DOWN in the next 15 seconds.

## 특징 / Features

- 🌏 한국어 / English 자동 감지 + 수동 전환
- 📈 실시간 BTC 시세: Binance WebSocket → Coinbase WebSocket → REST 폴백 (Binance / Coinbase / Kraken / CryptoCompare)
- 🎮 15초 예측 게임, 연승 스트릭 & 전적 저장 (localStorage)
- 🎉 승리 시 이모지 컨페티, 결과 공유 버튼
- ⚡ 비트코인 후원 모달 (QR 코드 + 주소 복사)
- 🧪 모든 시세 서버가 차단된 환경(사내망 등)에서는 자동으로 **시뮬레이션 모드** 전환 — 게임은 항상 플레이 가능

## ⚙️ 배포 전 필수 설정

[index.html](index.html) 상단의 후원 주소를 본인 비트코인 주소로 바꾸세요:

```js
const DONATION_ADDRESS = "YOUR_BTC_ADDRESS_HERE"; // ← 여기!
```

주소를 설정하지 않으면 후원 모달에 안내 문구만 표시됩니다 (잘못된 주소로 송금되는 사고 방지).

## 배포 / Deploy

빌드 과정 없는 단일 `index.html` — GitHub Pages에 바로 올리면 됩니다.

```bash
git init
git add .
git commit -m "Add Bitcoin prediction game"
# GitHub에 저장소 생성 후 push → Settings > Pages > main branch 선택
```

## 참고

- 실제 돈이 오가지 않는 재미용 게임입니다.
- 한국에서 Binance API가 차단된 경우에도 Coinbase/Kraken 폴백으로 동작합니다.
- 게임 시간은 `ROUND_SECONDS` 상수로 조절 가능 (기본 15초).
