# n8n-office-document
辦公室文件申請自動化系統

使用 n8n 建置辦公室文件申請流程。使用者填寫線上表單後，系統會自動將申請內容寄送至指定 Gmail，減少人工轉寄、複製資料與漏件風險。

## 專案功能

- 提供線上文件申請表單
- 收集申請人、部門、文件類型、完成期限與需求說明
- 自動將表單內容整理為 Email
- 透過 Gmail 寄送通知給承辦人
- 可延伸為案件編號、Google Sheets 紀錄、緊急案件通知與逾期提醒

## 流程圖

```mermaid
flowchart LR
    A["文件申請<br/>Form Trigger"] --> B["表單<br/>Next Form Page"]
    B --> C["產生申請編號<br/>Edit Fields"]
    C --> D["寄送 Gmail<br/>Send Message"]
    C --> E["儲存 Sheets<br/>Append Row"]
