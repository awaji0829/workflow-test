# React TypeScript 프로젝트 템플릿

## 1. 프로젝트 소개

이 프로젝트는 React와 TypeScript를 기반으로 한 프론트엔드 템플릿입니다. 모던 웹 개발에 필요한 다양한 기능과 도구들이 미리 설정되어 있어 빠른 개발이 가능합니다.

## 2. 기술 스택

- **핵심 프레임워크**

  - React 18.2.0
  - TypeScript 5.7
  - Vite 6

- **상태 관리**

  - Zustand (전역 상태 관리)
  - React Query DevTools (서버 상태 관리 디버깅)

- **스타일링**

  - Tailwind CSS
  - SCSS

- **라우팅**

  - React Router v7

- **API 통신**

  - Axios

- **개발 도구**
  - ESLint
  - Prettier
  - TypeScript ESLint

## 3. 프로젝트 구조

```
src/
├── 📁 api/                    # API 관련 파일
│   ├── 📁 auth/              # 인증 관련 API
│   │   ├── 📄 ApiAuth.ts     # API 함수 (sample)
│   │   └── 📄 ApiAuth.type.ts # API 타입 정의 (sample)
│   ├── 📁 common/            # 공통 API 타입
│   │   └── 📄 ApiCommon.type.ts (sample)
│   └── 📄 axios.ts           # Axios 인스턴스 설정
├── 📁 assets/                # 정적 리소스
│   ├── 📁 fonts/            # 폰트 파일
│   ├── 📁 images/           # 이미지 파일
│   └── 📁 styles/           # 전역 스타일
├── 📁 components/           # 공통 컴포넌트
│   ├── 📁 common/          # 범용 컴포넌트
│   ├── 📁 layout/          # 레이아웃 컴포넌트
│   └── 📁 ui/              # 기본 UI 컴포넌트
├── 📁 config/              # 설정 파일
│   └── 📄 env.ts           # 환경 변수 및 상수 설정
├── 📁 hooks/               # 커스텀 훅
├── 📁 pages/              # 페이지 컴포넌트
│   ├── 📁 about/          # 소개 페이지 (sample)
│   │   ├── 📄 AboutPage.tsx
│   │   └── 📁 components/  # 페이지 전용 컴포넌트
│   ├── 📁 dashboard/      # 대시보드 (sample)
│   │   ├── 📄 DashboardPage.tsx
│   │   └── 📁 components/  # 페이지 전용 컴포넌트
│   ├── 📁 home/           # 홈 페이지 (sample)
│   │   ├── 📄 HomePage.tsx
│   │   └── 📁 components/  # 페이지 전용 컴포넌트
│   ├── 📁 login/          # 로그인 페이지 (sample)
│   │   ├── 📄 LoginPage.tsx
│   │   └── 📁 components/  # 페이지 전용 컴포넌트
│   ├── 📁 not-found/      # 404 페이지 (sample)
│   │   ├── 📄 NotFoundPage.tsx
│   │   └── 📁 components/  # 페이지 전용 컴포넌트
│   └── 📁 sample-page/    # 샘플 페이지 (sample)
│       ├── 📄 SamplePage.tsx
│       └── 📁 components/  # 페이지 전용 컴포넌트
├── 📁 providers/          # React Context Provider 컴포넌트
├── 📁 router/             # 라우팅 관련 파일
│   └── 📄 AppRouter.tsx   # 라우터 설정
├── 📁 store/              # Zustand 스토어
│   ├── 📄 rootStore.ts    # 루트 스토어 설정
│   └── 📁 slices/        # 스토어 슬라이스
│       ├── 📄 authSlice.ts  # 인증 관련 상태
│       └── 📄 uiSlice.ts    # UI 관련 상태
├── 📁 types/             # 전역 타입 정의
│   ├── 📁 common/       # 공통 타입 정의 (sample)
│   └── 📁 pages/        # 페이지별 타입 정의 (sample)
├── 📁 utils/             # 유틸리티 함수
├── 📄 App.tsx            # 메인 애플리케이션 컴포넌트
├── 📄 main.tsx           # 애플리케이션 진입점
└── 📄 vite-env.d.ts      # Vite 타입 정의
```

## 4. 주요 기능

### 4.1 프로젝트 구조

- **페이지 기반 구조**

  - 각 페이지별 독립적인 디렉토리 구성
  - 페이지별 컴포넌트, 스타일, 로직 분리
  - 페이지 전용 컴포넌트는 해당 페이지 디렉토리 내 components 폴더에 위치
  - 라우팅 기반 코드 스플리팅

- **컴포넌트 구조**

  - UI: 기본 UI 컴포넌트 (버튼, 입력 필드 등)
  - Layout: 페이지 레이아웃 컴포넌트
  - Common: 재사용 가능한 범용 컴포넌트

- **설정 관리**

  - env.ts: 환경 변수, API 엔드포인트, 라우트 경로 등 상수 관리
  - 타입 안전한 환경 설정

- **리소스 관리**
  - assets 디렉토리에서 정적 리소스 체계적 관리
  - 폰트, 이미지, 스타일 파일 분리
  - 전역 스타일 및 테마 관리

### 4.2 API 통신 구조

- **도메인 기반 구조**

  - 각 도메인별로 폴더 분리 (auth, user 등)
  - API 함수와 타입 정의 분리

- **타입 시스템**

  - API 요청/응답 타입 정의
  - 공통 응답 타입 (BaseApiResponse)
  - 에러 처리 타입 (ApiErrorResponse)

- **Axios 인스턴스**
  - 인터셉터 설정
  - 토큰 관리
  - 에러 핸들링

### 4.3 상태 관리

- **Zustand 스토어**
  - rootStore: 전역 스토어 설정 및 초기화
  - 도메인별 슬라이스 분리 (auth, ui 등)
  - 영속성 미들웨어 (zustand-persist)
  - 타입 안정성

### 4.4 라우팅

- **React Router**
  - 중첩 라우팅
  - 권한 기반 접근 제어
  - 레이아웃 시스템

## 5. 시작하기

### 5.1 설치

```bash
# 의존성 설치
npm install

# 개발 서버 실행
npm run dev

# 빌드
npm run build
```

### 5.2 환경 변수

```env
# .env
VITE_API_BASE_URL=http://localhost:3000
```

## 6. 개발 가이드

### 6.1 API 통신

```typescript
// API 함수 정의
import { apiClient } from '@/api/axios';
import { ApiLoginRequest, ApiLoginResponse } from '@/api/auth/ApiAuth.type';

export const authApi = {
  login: (data: ApiLoginRequest) => {
    return apiClient.post<ApiLoginResponse>('/auth/login', data);
  },
};

// API 사용
const response = await authApi.login({ username, password });
```

### 6.2 상태 관리

```typescript
// 스토어 슬라이스 정의
import { create } from 'zustand';
import { persist } from 'zustand/middleware';
import { ApiLoginRequest } from '@/api/auth/ApiAuth.type';

interface AuthState {
  user: User | null;
  login: (data: ApiLoginRequest) => Promise<void>;
}

export const useAuthStore = create<AuthState>()(
  persist(
    (set) => ({
      user: null,
      login: async (data) => {
        // 로그인 로직
      },
    }),
    {
      name: 'auth-storage',
    },
  ),
);
```

## 7. 배포

### 7.1 빌드

```bash
npm run build
```
