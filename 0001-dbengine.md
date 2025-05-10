# 1. DBEngine

Date: 2025-05-09

## Status

Superceded by [2. DBEngine-serverless](0002-dbengine-serverless.md)

## Context
- マルチテナント環境を前提として使用するため、自動的にスケーリングされるのが望ましい
- リリース後の保守・運用面での容易性
- テクノロジを学習するコストも無視できない
- できる限り冗長性を高めたい

## Decision
- Amazon Aurora PostgreSQLを採用
- Amazon Auroraは、Serverlessを選択する

## Consequences
- Amazon Aurora PostgreSQLを採用することで、スケーリングについて自動化が実現される
- また、リリース後の保守・運用面での容易性についてもある程度予見可能となり、学習コストも極小化される
- 比較検討したDynamoDBと比べて、冗長性は劣るが、開発対象のサービスにおいては十分なサービスレベルを保証可能であると判断する
- Serverlessは、自動的に起動、シャットダウン、および容量をスケールアップまたはスケールダウンする