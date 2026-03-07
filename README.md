# ALICE-Secure-Network

Zero-trust network infrastructure with encrypted DNS, auth, and edge caching

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-dns, alice-crypto, alice-auth, alice-edge, alice-cache

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/resolve` | 暗号化DNS解決 |
| `POST` | `/api/v1/authenticate` | ゼロトラスト認証 |
| `GET ` | `/api/v1/policies` | セキュリティポリシー一覧 |
| `GET ` | `/api/v1/audit` | 監査ログ |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
