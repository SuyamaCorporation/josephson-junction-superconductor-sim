# Josephson Junction Superconductor Simulation

## 概要
ジョセフソン接合を流れるクーパー対のトンネル電流をRSJ（Resistively Shunted Junction）モデルで数値積分し、AC/DCジョセフソン効果と電流-電圧特性曲線をリアルタイム描画するシミュレーター。

## 機能
- Canvas上にI-V特性曲線をリアルタイム描画（DC分岐：緑、AC分岐：黄）
- 位相φ(t)と電圧V(t)の時間発展グラフをCanvas描画
- バイアス電流 I_b/I_c（0〜2）とダンピングパラメータ β_c（0.1〜10）のスライダー制御
- 第4次ルンゲ・クッタ法による数値積分（RSJモデル）
- DC/ACジョセフソン効果の自動判定と説明表示
- ジョセフソン周波数 f_J = 2eV/h のリアルタイム計算
- I_c、平均電圧、超電流、位相値のライブ計測値表示
- I-V特性スイープ機能（β_c変化時に自動再計算）

## 使い方
1. スライダーで I_b/I_c を設定（< 1.0: DCジョセフソン効果、> 1.0: ACジョセフソン効果）
2. β_c（Stewart-McCumberパラメータ）でダンピング特性を調整
3. `I-V Sweep` ボタンでI-V曲線全体を再計算
4. `⏸ Pause` / `▶ Run` でシミュレーション停止/再開
5. `↺ Reset` で初期化

## 技術スタック
- Pure HTML/CSS/JavaScript
- Tailwind CSS (CDN)
- Canvas 2D API による動的グラフ描画
- 4次ルンゲ・クッタ数値積分
