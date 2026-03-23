RHCSA Lab Log
RHCSA 자격증 준비 및 Linux 시스템 관리 실습 과정을 기록한 문서입니다.
VMware 기반 Red Hat Enterprise Linux 환경에서 실습을 진행하고 있습니다.

🧪 Lab Environment
OS: Red Hat Enterprise Linux 10
Virtualization: VMware Workstation
접속 방식: SSH

Day04 (Node1 System Configuration)

## 📌 Overview

RHCSA 실습 환경(Node1)을 기반으로 시스템 초기 구성 및 서비스 관리 작업을 수행하였습니다.
이번 실습에서는 실제 시험에서 요구되는 Linux 시스템 관리 흐름을 따라 네트워크 구성, 패키지 저장소 설정, 보안 정책 조정, 사용자 권한 관리, 그리고 작업 자동화를 중심으로 실습을 진행하였습니다.

---

## 🖥 Network Configuration

시스템 식별을 위해 호스트네임을 변경하고 정적 IPv4 네트워크 환경을 구성하였습니다.
IP 주소, 게이트웨이, DNS 정보를 직접 설정하여 서버가 안정적으로 네트워크에 연결되도록 구성하였으며, 정상 적용 여부를 확인하였습니다.

---

## 📦 Package Repository Configuration

로컬 환경에서 제공된 경로를 기반으로 BaseOS와 AppStream 저장소를 직접 구성하였습니다.
저장소 메타데이터를 갱신하여 패키지 관리 시스템이 정상적으로 동작하도록 설정하였습니다.

---

## 🔐 SELinux & Web Service Troubleshooting

웹 서버가 기본 포트가 아닌 비표준 포트에서 동작하도록 요구 조건을 분석하였습니다.
SELinux 정책을 조정하여 웹 서비스 포트를 허용하고, 웹 서버 설정 및 방화벽 규칙을 함께 수정하였습니다.
또한 서비스가 시스템 재부팅 이후에도 자동으로 실행되도록 설정한 뒤 정상적인 서비스 제공 여부를 검증하였습니다.

---

## 👥 User and Privilege Management

관리 목적의 그룹을 생성하고 여러 사용자 계정을 요구 조건에 맞게 구성하였습니다.
일부 계정에는 보조 그룹 권한을 부여하였으며, 특정 계정은 로그인이 제한된 형태로 생성하였습니다.
sudo 정책을 활용하여 그룹 단위 관리 권한을 위임하고, 특정 사용자에게는 제한된 명령을 비밀번호 입력 없이 수행할 수 있도록 권한을 세분화하였습니다.

---

## ⏱ Task Automation (Cron)

cron 서비스를 활성화하고 특정 사용자 기준의 반복 작업을 설정하였습니다.
주기적으로 시스템 로그가 기록되도록 자동화 작업을 구성하여 스케줄링 기능의 정상 동작을 확인하였습니다.

---

## ✅ Key Takeaways

* Linux 서버의 기본 네트워크 구성 절차를 이해하였습니다.
* YUM Repository 수동 구성 과정을 경험하였습니다.
* SELinux 정책과 서비스 동작 간의 관계를 실습을 통해 확인하였습니다.
* 사용자 및 sudo 권한 관리 방식을 학습하였습니다.
* cron 기반 작업 자동화 개념을 적용해 보았습니다.
