# 다운로드 버튼 시인성 개선 - 설계

## 현재 상태
- 두 버튼 모두 `bg-white text-gray-700 border-gray-200` — 주변 UI와 동화되어 눈에 띄지 않음

## 변경 방안
### 엑셀 버튼
- 활성: `bg-emerald-600 text-white border-emerald-600 hover:bg-emerald-700`
- 비활성: `opacity-40 cursor-not-allowed bg-emerald-600 text-white`
- 아이콘: `stroke="white"`로 변경 (currentColor 유지하면 자동 적용)

### PDF 버튼
- 활성: `bg-red-600 text-white border-red-600 hover:bg-red-700`
- 비활성: `opacity-40 cursor-not-allowed bg-red-600 text-white`
- 아이콘: 동일하게 currentColor로 자동 적용

## 수정 파일
- `src/components/DownloadButtons.tsx` — className만 변경, 로직 변경 없음
