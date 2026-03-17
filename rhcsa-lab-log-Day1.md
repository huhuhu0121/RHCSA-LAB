# RHCSA Lab Log

RHCSA 자격증 준비 및 Linux 시스템 관리 실습 과정을 기록한 문서입니다.  
VMware 기반 Red Hat Enterprise Linux 환경에서 실습을 진행하고 있습니다.

---

## 🧪 Lab Environment
- OS: Red Hat Enterprise Linux 9
- Virtualization: VMware Workstation
- 접속 방식: SSH

---

# 📅 Day 01 - RHEL Installation & Basic Setup

## 🎯 목표
- RHEL 설치 및 기본 환경 구성
- SSH 접속 설정

## 💻 실습 내용
- VMware에 가상 머신 생성
- RHEL 설치 완료
- 네트워크 설정 및 IP 확인
- SSH 접속 테스트 진행

## ⚠ 문제 상황
- SSH 접속 불가

## 🔍 해결 과정
1. SSH 서비스 상태 확인
   systemctl status sshd

## 🔍 서비스 실행
  systemctl start sshd  

## 🔍 방화벽 설정 확인 및 SSH 허용
  firewall-cmd --add-service=ssh --permanent
  firewall-cmd --reload

## ✅ 결과
  SSH 접속 성공
  기본 서버 환경 구축 완료

## 💡 배운 점
  서비스 상태와 방화벽 설정을 함께 확인해야 함
