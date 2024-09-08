# Front-End Ground Rule

## Naming

### 1. Folder

- `lowercase`
- (ex: /components)

### 2. File

- 컴포넌트 → `PascalCase`
- 함수 → `camelCase`

### 3. Page

- `lowercase`
- (ex: /home/hi)

## 기술 스택

- React (18)
- Next.js (14.0.4) - Page routing
- Typescript version 5

## Commit Convention

```c
 ex) feat: 구현한 내용 (한글 or 영어)
```

- **`feat`** : 새로운 기능 추가
- **`fix`** : 오류(버그) 수정
- **`style`** : 코드가 변하지 않는 수정 ex) 세미콜론, 들여 쓰기
- **`refactor`** : 코드의 리팩토링
- **`test`** : test 코드 삽입 및 수정
- **`design`** : css, ui 변경
- **`rename`** : 파일명/폴더명 변경
- **`remove`** : 파일 삭제
- **`comment`** : 필요한 주석 추가 및 변경
- **`chore`** : 빌드 혹은 패키지 매니저 수정사항

## PR Convention

```c
 제목 ex) [Feat] 구현한 내용
```

- ** pr템플릿 만들어 둘 예정입니다!

- PR 올리면 PR리뷰 달아주기
- 확인이 다 끝나면 Approve 해주기
- Comment 반영 완료 이후 Merge 하기

## Branch Naming

```c
 ex) feat/login
```

- feat/ → 새로운 기능을 추가할 때
- fix/ → 오류 난 것을 고칠 때
- refactor/ → 최적화할때
- style/ → 디자인 수정

### 브랜치 전략

1. main branch를 checkout 합니다.
2. feature branch를 각자 만듭니다.
3. feature branch에서 각자 개발합니다.
4. 개발이 끝나면 PR을 올립니다.
5. PR리뷰 반영 이후 feature branch를 main branch와 합칩니다(merge).
- `main` : 프로젝트 최종 브랜치, 해당 브랜치로 배포

## 기타 개발 컨벤션

- 파일 import시 절대 경로 사용
- prettier, eslint 사용 (*제가 세팅 해둘게요!)
- 페이지, 컴포넌트는 function(함수 선언문)으로, 기타 함수들은 화살표 함수로

```jsx
 function Button({ imageUrl, children }: ButtonProps) { // 페이지, 컴포넌트는 함수 선언문으로!

  const handleClick = () => {} // Component 내의 함수는 화살표 함수로!
  
  return (
    <div>
      {children}
    </div>
  )
}

export default Button;
```
