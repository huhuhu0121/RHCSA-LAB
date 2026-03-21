---

# 📅 Day 03 - Service Management (systemctl)

## 🎯 목표
- systemctl을 이용한 서비스 관리 방법 이해
- 서비스 시작, 중지, 자동 실행 설정 학습
- 서비스 상태 확인 및 문제 해결 경험

## 💻 실습 내용
- 서비스 상태 확인
  systemctl status sshd

- 서비스 시작 및 중지
  systemctl start sshd
  systemctl stop sshd

- 서비스 재시작
  systemctl restart sshd

- 부팅 시 자동 실행 설정
  systemctl enable sshd

- 자동 실행 해제
  systemctl disable sshd

- 활성화 여부 확인
  systemctl is-enabled sshd

## ⚠ 문제 상황
- 서비스 실행 후 외부 SSH 접속이 되지 않음

## 🔍 해결 과정
1. 서비스 상태 확인
   systemctl status sshd

2. 서비스는 실행 중(active) 상태 확인

3. 방화벽 설정 확인
   firewall-cmd --list-all

4. SSH 서비스 허용
   firewall-cmd --add-service=ssh --permanent
   firewall-cmd --reload

5. 접속 재시도 후 정상 연결 확인

## ✅ 결과
- systemctl 명령어를 이용해 서비스 제어 가능
- 부팅 시 SSH 자동 실행 설정 완료
- 서비스 문제 발생 시 확인 절차 이해

## 💡 배운 점
- 서비스 실행 여부와 네트워크 접근 가능 여부는 별개의 문제일 수 있음
- 문제 발생 시 서비스 상태 → 방화벽 → 네트워크 순서로 확인하는 것이 효율적임
