# 1. DBEngine

Date: 2025-05-09

## Status

Accepted

## Context
- マルチテナント環境を前提として使用するため、自動的にスケーリングされるのが望ましい
- リリース後の保守・運用面での容易性
- テクノロジを学習するコストも無視できない
The issue motivating this decision, and any context that influences or constrains the decision.

## Decision
- Amazon Aurora PostgreSQLを採用

## Consequences
- Amazon Aurora PostgreSQLを採用することで、スケーリングについて自動化が実現される
- また、リリース後の保守・運用面での容易性についてもある程度予見可能となり、学習コストも極小化される
- 比較検討したDynamoDBと比べて、冗長性は劣るが、開発対象のサービスにおいては十分なサービスレベルを保証可能であると判断する