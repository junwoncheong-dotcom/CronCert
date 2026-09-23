# CronCert

SSL Certificate & API Key Expiration Alert via Slack/Telegram

## 🚀 Project Overview
1인 AI 서비스(SaaS) 인프라의 안정적인 운영을 위한 모니터링 시스템입니다. 
외부 API 키 및 SSL 인증서 만료일을 주기적으로 체크하여 만료 전에 알림을 발송합니다.

## 🛠️ Monitoring Targets
- **SSL Certificates**: 서비스 도메인 보안 인증서 만료일
- **API Keys**: 
  - Supabase Project (`cert-doberman`) API Key 및 JWT 만료 관리
  - TypeSafe AI (Jev 1.13) API 크레딧 및 연동 키 체크

## ⚙️ Environment Variables (.env)
시스템 가동을 위해 아래 환경변수 설정이 필요합니다.
- `SUPABASE_KEY`: cert-doberman 프로젝트 접근 키
- `JEV_API_KEY`: TypeSafe AI API 인증 키
- `SLACK_WEBHOOK_URL`: 알림을 받을 슬랙 채널 웹훅 주소

## ⏰ Cron Schedule
- 매일 오전 09:00 (KST) 자동 스크리닝 및 얼럿 체크
