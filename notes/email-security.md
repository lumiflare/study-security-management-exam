# メールセキュリティ

## 送信ドメイン認証（サーバ間）
- SPF: 送信元IPをDNSで検証（IPの正当性）
- DKIM: デジタル署名でメール内容の改ざん検知
- DMARC: SPF+DKIMの統合ポリシー（失敗時の処理: none/quarantine/reject）

## メール暗号化・署名（エンドツーエンド）
- S/MIME: CA（認証局）による証明書、企業向け
- PGP: Web of Trust（利用者間の信頼）、CA不要、個人向け
- 両方とも暗号化（機密性）＋デジタル署名（認証・改ざん検知）が可能

## その他
- SMTP over TLS（STARTTLS）: サーバ間通信の暗号化
- PPAP（PW付ZIP＋別送PW）: 安全でないため廃止傾向
