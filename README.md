# 에딩턴 한계광도 계산기

복사 가속도와 중력가속도가 같은 구대칭 에딩턴 광도 척도를 계산한다.

- ID: E107
- App: https://nanalab.kr/eng-eddington-luminosity/
- Repository: https://github.com/NaNaCompany/eng-eddington-luminosity
- Formula: L_Edd = 4πGMc/κ

## Model and data

M,κ>0. κ는 복사 운동량 전달에 쓰는 일정한 유효 질량 불투명도(m²/kg)이며 길이당 흡수계수와 다르다. 구대칭·등방 복사·정상상태·뉴턴 중력과 물질-복사 결합을 가정한다. 전자 산란 예시 κ=0.034 m²/kg를 제공하지만 물성표나 조성을 자동 추정하지 않는다. 회전·자기장·비등방 방출·대류·일반상대론을 제외한다. 모든 천체에 대한 절대 광도 상한이 아니다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
