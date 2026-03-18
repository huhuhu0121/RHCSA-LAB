---
# RHCSA Lab Log

RHCSA 자격증 준비 및 Linux 시스템 관리 실습 과정을 기록한 문서입니다.  
VMware 기반 Red Hat Enterprise Linux 환경에서 실습을 진행하고 있습니다.

---

## 🧪 Lab Environment
- OS: Red Hat Enterprise Linux 9
- Virtualization: VMware Workstation
- 접속 방식: SSH

---
# 📅 Day 02 - User & Permission Management

## 🎯 목표
- Linux 사용자 및 그룹 관리 이해
- 파일 권한과 소유권 개념 학습
- RHCSA 필수 명령어 익히기

## 💻 실습 내용
- 사용자 생성 및 비밀번호 설정
  useradd testuser
  passwd testuser

- 그룹 생성 및 사용자 추가
  groupadd devgroup
  usermod -aG devgroup testuser

- 사용자 정보 확인
  id testuser

- 파일 권한 확인
  ls -l

- 권한 변경
  chmod 755 testfile

- 소유자 변경
  chown testuser:devgroup testfile

## ⚠ 문제 상황
- 생성한 사용자가 파일에 접근하지 못함

## 🔍 해결 과정
1. 파일 권한 확인
   ls -l testfile

2. 소유자가 root로 설정되어 있는 것을 확인

3. 소유자 변경
   chown testuser:devgroup testfile

4. 권한 재설정
   chmod 755 testfile

## ✅ 결과
- 사용자 계정 정상 생성
- 그룹 권한 적용 확인
- 파일 접근 정상 동작

## 💡 배운 점
- Linux에서는 사용자(User), 그룹(Group), 권한(Permission)이 함께 동작함
- 권한 문제 발생 시 ls -l 로 상태 확인이 가장 먼저 필요함
