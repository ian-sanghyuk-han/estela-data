# estela-data

**[Estela](https://github.com/ian-sanghyuk-han/estela)의 등기부 자료.** 앱이 여기서 읽어 갑니다.

앱과 자료를 갈라 둔 이유는 용량이 아니라 **갱신**입니다. Overture는 매달 새 판이 나오는데,
한 저장소에 같이 있으면 갱신 한 번에 수백 MB가 앱 이력에 영구히 쌓입니다.
갈라 두면 앱 저장소는 가볍게 남고, 자료는 얼마든지 다시 만들 수 있습니다.

## 무엇이 들어 있나

`registry/manifest.json` 하나와 `registry/<출처>/<칸>.json` 여럿.
칸은 0.01°~0.25°짜리 격자이고, 브라우저는 **화면에 걸친 칸만** 받아 갑니다 —
전체를 내려받는 일은 없습니다.

- **정부 명부** — 각국이 내는 식품업 면허·위생점검 등록부. 위생 등급과 점수는
  일부러 버렸습니다. 그건 국가의 판단이고, Estela는 누구의 판단도 싣지 않습니다.
  존재한다는 사실과 업종만 가져옵니다.
- **Overture Maps** — 정부 명부가 없는 나라를 메웁니다. CDLA Permissive 2.0 / Apache 2.0.
  OpenStreetMap 자료는 들어 있지 않습니다(ODbL 전염 없음).

출처마다 `source`·`license`·`lastVerified`가 manifest에 적혀 있습니다.

## 만드는 법

앱 저장소의 `tools/harvest_overture.py`. 왜 그렇게 생겼는지는 그쪽 `tools/README.md`와
`docs/place-registries.md`에 적혀 있습니다.

## 라이선스

자료마다 다릅니다 — manifest의 `license` 항목을 보십시오.
이 저장소의 문서와 구성은 앱과 같은 조건을 따릅니다.
