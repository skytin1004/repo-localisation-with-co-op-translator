<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "063bf29dec5487cc1aeaba73b92963cf",
  "translation_date": "2026-01-12T19:36:16+00:00",
  "source_file": "README.md",
  "language_code": "ko"
}
-->
# 저장소 현지화 데모 (Co-op Translator + GitHub Actions)

이것은 바로 이런 종류의 편집입니다

이 저장소는 문서 현지화를 자동화하는 **라이브 데모**로 설정되어 있습니다:

- Markdown 파일(예: `README.md`)을 편집합니다
- `main` 브랜치에 푸시합니다
- GitHub Actions가 Co-op Translator를 실행합니다
- 번역된 결과가 `translations/<lang>/...` 경로에 생성/업데이트됩니다
- 변경 사항에 대한 **풀 리퀘스트**가 열려 리뷰할 수 있습니다

아래는 Co-op Translator의 테스트 이미지입니다.

![Co-op Translator Test Image](../../translated_images/ko/co-op-translator-test.51ff3a819e57ea39.png)

## 포함된 항목

- **문서**: `README.md`, `docs/`
- **자동화**: `.github/workflows/co-op-translator.yml`

## 사전 준비 사항 (GitHub Secrets)

**Settings → Secrets and variables → Actions**에서 아래를 추가하세요:

- **`OPENAI_API_KEY`**: OpenAI API 키

나중에 이미지 번역을 원하시면 Azure AI Vision 비밀 값도 추가하고(선택 사항), `.github/workflows/translate.yml`에서 `-img`를 활성화하세요.

## 데모 진행 흐름 (무대에서 할 일)

1. `README.md`(또는 `docs/` 내 파일)에서 한 줄을 편집합니다
2. 커밋 후 `main`에 푸시합니다
3. **Actions** 탭을 열어 워크플로 실행을 보여줍니다
4. 생성된 **풀 리퀘스트**를 엽니다
5. `translations/ko/` (및 활성화된 경우 다른 언어들)에서 변경 사항을 보여줍니다

## 지원 언어

워크플로 기본 언어:

- 한국어: `ko`
- 일본어: `ja`
- 프랑스어: `fr`

`.github/workflows/co-op-translator.yml`에서 변경 가능합니다.

## 참고 사항

- Co-op Translator 프로젝트: `https://github.com/Azure/co-op-translator`

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**면책 조항**:  
이 문서는 AI 번역 서비스 [Co-op Translator](https://github.com/Azure/co-op-translator)를 사용하여 번역되었습니다. 정확성을 위해 최선을 다하고 있지만, 자동 번역에는 오류나 부정확한 부분이 있을 수 있음을 알려드립니다. 원문 문서는 해당 언어의 공식 출처로 간주되어야 합니다. 중요한 정보에 대해서는 전문적인 인간 번역을 권장합니다. 본 번역 사용으로 인해 발생하는 오해나 잘못된 해석에 대해 당사는 어떠한 책임도 지지 않습니다.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->