
# 작업 관리 CLI 애플리케이션

이 프로젝트는 작업을 관리할 수 있는 간단한 명령줄 인터페이스(CLI) 애플리케이션입니다.  
작업을 조회하고, 완료 처리하며, 삭제할 수 있는 기능을 제공합니다.

---

## 주요 기능

1. **작업 조회**  
   - 현재 등록된 모든 작업과 상태(완료/미완료)를 확인할 수 있습니다.
2. **작업 완료**  
   - 선택한 작업을 완료 상태로 변경합니다.
3. **작업 삭제**  
   - 선택한 작업을 삭제합니다.

---

## 동작 방식

### 1. 작업 조회
현재 등록된 작업을 번호와 상태와 함께 출력합니다.  
만약 등록된 작업이 없다면 메시지를 출력합니다.

```python
def view_tasks():
    tasks = load_tasks()  # 작업 목록 불러오기
    if not tasks:
        print("현재 등록된 작업이 없습니다.")
    else:
        print("작업 목록:")
        for idx, task in enumerate(tasks, start=1):
            status = "완료" if task['completed'] else "미완료"
            print(f"{idx}. {task['name']} - {status}")
```
---

### 2. 작업 완료 처리
작업 번호를 입력받아 해당 작업을 완료 상태로 변경합니다.

```python
def complete_task(task_number):
    tasks = load_tasks()
    if 1 <= task_number <= len(tasks):
        tasks[task_number - 1]['completed'] = True
        save_tasks(tasks)
        print(f"작업 '{tasks[task_number - 1]['name']}'이(가) 완료 처리되었습니다.")
    else:
        print("유효하지 않은 작업 번호입니다. 다시 확인해주세요.")
```
---

### 3. 작업 삭제
작업 번호를 입력받아 해당 작업을 삭제합니다.

```python
def delete_task(task_number):
    tasks = load_tasks()
    if 1 <= task_number <= len(tasks):
        deleted_task = tasks.pop(task_number - 1)
        save_tasks(tasks)
        print(f"작업 '{deleted_task['name']}'이(가) 삭제되었습니다.")
    else:
        print("유효하지 않은 작업 번호입니다. 다시 확인해주세요.")
```

---

## 시작하기

1. 레포지토리 클론:
    ```bash
    git clone https://github.com/yourusername/yourrepository.git
    cd yourrepository
    ```

2. 의존성 설치 (필요할 경우):
    ```bash
    pip install -r requirements.txt
    ```

3. 애플리케이션 실행:
    ```bash
    python main.py
    ```

---

## 예제 사용 방법

### 작업 조회
```plaintext
현재 등록된 작업이 없습니다.
```

### 작업 추가 (예시)
작업 추가 기능은 아래와 같이 구현 가능합니다:
```python
def add_task(task_name):
    tasks = load_tasks()
    tasks.append({'name': task_name, 'completed': False})
    save_tasks(tasks)
    print(f"작업 '{task_name}'이(가) 추가되었습니다.")
```

### 작업 완료 처리
```plaintext
작업 '청소하기'이(가) 완료 처리되었습니다.
```

### 작업 삭제
```plaintext
작업 '청소하기'이(가) 삭제되었습니다.
```

---

## 작동 영상

![작동 데모](path/to/demo-video.gif)

---

## 기여하기

이 프로젝트에 기여하고 싶으신 분들은 환영합니다!  
풀 리퀘스트를 생성하거나 이슈를 열어 의견을 나눠주세요.

---

## 라이선스

이 프로젝트는 MIT 라이선스를 따릅니다.
