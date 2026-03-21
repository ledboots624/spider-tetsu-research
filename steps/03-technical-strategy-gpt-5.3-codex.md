# スパイダーテツ情報共有プロジェクト：技術戦略・アクションプラン

## 優先順位付き施策（実現可能性・リスク評価）

| ID | 施策（主張） | 優先度 | 実現可能性 | 主なリスク | 技術アクション | 信頼度 | source_type | source_title | source_locator | access_date | reliability_tier | primary_source |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| S1 | 経歴・海外経験・ライブ・機材を一元管理する「証拠付きナレッジDB」が必要 | P0 | 高 | 初期データ整理工数 | `content`と`source`を分離し、各記事に`source_id/reliability_tier/confidence`を必須化 | high | unknown | User-provided research_scope JSON（focus指定） | N/A | 2026-03-21 | tier1 | false |
| S2 | 一次情報とコミュニティ情報の混在に対応する真偽ラベル運用が必要 | P0 | 高 | 表記基準の不統一 | 公開面に「公式確認済み/コミュニティ証言/未検証」バッジを実装。争点情報は注釈付き表示 | high | community_data | 深層分析レポート（Otis Rush共演のエビデンス評価） | https://spider-tetsu.jimdosite.com/spider-tetsu/ | 2026-03-21 | tier2 | false |
| S3 | 10ページ共有資料を最初のMVP成果物にするべき | P0 | 高 | テンプレ固定時の柔軟性不足 | 10ページの固定テンプレを作成し、DBから自動差し込みで更新 | high | community_data | 深層分析レポート 7章（10ページ構成提案） | https://spider-tetsu.jimdosite.com/ / https://lit.link/spidertetsu | 2026-03-21 | tier2 | false |
| S4 | ライブ中心の情報体験（予定＋履歴）を中核機能に置くべき | P0 | 高 | 更新停止 | 週次更新のライブカレンダーと過去公演アーカイブを同時運用 | high | official_document | Spider Tetsu lit.link（スケジュール情報） | https://lit.link/spidertetsu | 2026-03-21 | tier1 | true |
| S5 | 機材・音作り特集はファン深耕に有効 | P1 | 高 | 情報の古さ | Spider-H、使用ギター、アンプの「検証済み機材ページ」を作る | high | industry_report | K&T MODERN VINTAGE GUITARS - SPIDER-H Product Page | https://www.kt-pickup.com/product/spider-h-set/ | 2026-03-21 | tier1 | true |
| S6 | ファン投稿は「投稿→検証→公開」の審査フローが必須 | P1 | 中 | 誤情報・荒れ | 投稿フォーム、レビューキュー、差し戻し理由テンプレを実装 | medium | unknown | User-provided research_scope JSON（purpose: ファンで情報共有） | N/A | 2026-03-21 | tier1 | false |
| S7 | 海外経験を踏まえ、JP/EN二言語化は第2段階で有効 | P2 | 中 | 翻訳品質 | まず固定ページのみ二言語化し、ライブ速報はJP優先で段階拡張 | medium | official_document | Spider Tetsu Official Website - Profile（シカゴ活動） | https://spider-tetsu.jimdosite.com/spider-tetsu/ | 2026-03-21 | tier1 | true |

## 実装ロードマップ（12週間）

| フェーズ | 期間 | 実装内容 | 完了条件 | 信頼度 | source_type | source_title | source_locator | access_date | reliability_tier | primary_source |
|---|---|---|---|---|---|---|---|---|---|---|
| R1 | 1-2週 | データモデル設計、既存情報の初期投入、真偽ラベル運用開始 | 主要トピック（経歴/海外/ライブ/機材）を最低1周公開可能 | medium | unknown | 技術戦略上の実装見積（MVP計画） | N/A | 2026-03-21 | tier4 | false |
| R2 | 3-5週 | Web MVP公開、10ページ資料テンプレ公開、ライブ予定連携 | ファン共有会で実際に使える状態 | medium | unknown | 技術戦略上の実装見積（MVP計画） | N/A | 2026-03-21 | tier4 | false |
| R3 | 6-8週 | ファン投稿導線、編集審査、改訂履歴管理 | 投稿から公開までの運用が回る | low | unknown | 技術戦略上の実装見積（運用拡張） | N/A | 2026-03-21 | tier4 | false |
| R4 | 9-12週 | JP/EN対応、分析計測、SNS配信用素材自動化 | 継続運用のKPI計測が可能 | low | unknown | 技術戦略上の実装見積（拡張計画） | N/A | 2026-03-21 | tier4 | false |

## 主要リスクと対策

| リスク | 影響 | 優先度 | 対策 | 信頼度 | source_type | source_title | source_locator | access_date | reliability_tier | primary_source |
|---|---|---|---|---|---|---|---|---|---|---|
| 事実の過剰断定（例：録音が残らない共演エピソード） | 信頼失墜 | 高 | 断定表現を避け、出典と確度を常時表示 | high | community_data | 深層分析レポート（エビデンス評価） | https://spider-tetsu.jimdosite.com/spider-tetsu/ | 2026-03-21 | tier2 | false |
| 写真・動画・音源の権利不備 | 公開停止・クレーム | 高 | 権利台帳（権利者/許諾範囲/期限）を必須化 | medium | unknown | 権利管理の一般実務知見 | N/A | 2026-03-21 | tier4 | false |
| ライブ情報の更新滞留 | 利用離脱 | 高 | 更新担当固定、週次SLA、未更新アラート | medium | official_document | Spider Tetsu lit.link（継続的スケジュール更新の必要性） | https://lit.link/spidertetsu | 2026-03-21 | tier1 | true |
| 投稿コミュニティの品質低下 | 炎上・離脱 | 中 | 投稿ガイドライン、モデレーション基準、通報導線 | medium | unknown | ファンコミュニティ運用上の一般知見 | N/A | 2026-03-21 | tier4 | false |