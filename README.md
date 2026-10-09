# Division Template Decisions (HOI4 MOD)

ディシジョンで新しい師団テンプレートを追加し、その師団を配置します。

| ディシジョン | 効果 |
| --- | --- |
| 歩兵師団テンプレートを追加 | テンプレート「Infantry Division 12」を追加、初期野戦砲・支援装備・工兵・騎兵偵察の技術を習得 |
| 騎兵師団テンプレートを追加 | テンプレート「Cavalry Division 12」を追加、初期野戦砲・支援装備・工兵・騎兵偵察の技術を習得 |
| 砲兵師団テンプレートを追加 | テンプレート「Artillery Division 16」を追加、初期野戦砲・支援装備・工兵・騎兵偵察の技術を習得 |
| 自動車化師団テンプレートを追加 | テンプレート「Motorized Division 16」を追加、初期野戦砲・支援装備・工兵・偵察中隊・自動車化歩兵の技術を習得 |
| 歩兵師団を配置 | 「Infantry Division 12」の師団を首都に24個配置 |
| 騎兵師団を配置 | 「Cavalry Division 12」の師団を首都に24個配置 |
| 砲兵師団を配置 | 「Artillery Division 16」の師団を首都に24個配置 |
| 自動車化師団を配置 | 「Motorized Division 16」の師団を首都に24個配置 |

## テンプレート構成

| テンプレート | 戦闘大隊 | 支援中隊 |
| --- | --- | --- |
| Infantry Division 12 | 歩兵大隊 ×12（4個×3列） | 砲兵・工兵・騎兵偵察 |
| Cavalry Division 12 | 騎兵大隊 ×12（4個×3列） | 砲兵・工兵・騎兵偵察 |
| Artillery Division 16 | 砲兵大隊 ×8（4個×2列）＋歩兵大隊 ×8（4個×2列） | 砲兵・工兵・騎兵偵察 |
| Motorized Division 16 | 自動車化歩兵大隊 ×8（4個×2列）＋自動車化砲兵大隊 ×8（4個×2列） | 砲兵・工兵・自動車化偵察 |

- テンプレート追加は、同名テンプレートがない場合のみ実行可能（削除すれば再追加可）
- 配置はテンプレートが存在し、首都を支配している場合のみ実行可能。何度でも実行可能
- 配置される師団は装備充足 100%・経験値最大（`start_experience_factor = 1.0`）で生成されます（備蓄の装備は消費しません）
- 政治力コスト 0、AI は使用しません

## インストール

1. このリポジトリを `Documents/Paradox Interactive/Hearts of Iron IV/mod/division_templates/` に配置
2. 同じ `mod` フォルダに `division_templates.mod` を作成し、以下を記述

```
version="1.0.0"
tags={
	"Gameplay"
	"Military"
}
name="Division Template Decisions"
supported_version="1.*"
path="mod/division_templates"
```

3. ランチャーで MOD を有効化

## 構成

```
descriptor.mod
common/decisions/categories/division_templates_categories.txt
common/decisions/division_templates_decisions.txt
localisation/english/division_templates_l_english.yml   (UTF-8 BOM付き)
```
