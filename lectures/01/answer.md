# 第1回 解答

## 演習

- 講座に固有の質問（宿題の3レベル）へのモデルの回答（要約でよい）：
- 用語集の正しい意味と比べて気づいたこと：
- 表示できたトークン数（入力 / 出力）：

## 宿題

- 取り組んだレベル：基礎
- やったこと：モデルを3つ切り替えて出力を確認した。(gemini-3.1-flash-lite,gemini-3.6-flash,gemini-3.8-flash)
- 結果：
    gemini-3.1-flash-lite:概要、背景、イメージ、メリット、まとめ
    gemini-3.6-flash:gemini-3.1-flash-lite+活用例
    gemini-3.8-flash:gemini-3.6-flash+技術的な仕組み
    概ね3つのモデルとも回答内容は同様であった。
- 気づき・疑問：
    3つのモデルともinput_tokens=7
    output_tokensはそれぞれ以下のとおりになった。
        gemini-3.1-flash-lite:645
        gemini-3.6-flash:817
        gemini-3.8-flash:814
    今回はgemini-3.6-flashが出力トークンが一番多い結果となった。
    作業環境が影響しているか不明だがgemini-3.1-flash-liteは、最後のまとめ部分が途中で途切れてしまっていた。
    もう一度gemini-3.1-flash-liteで同一の入力を与えたところ、まとめ部分の最後まで出力された。このときのoutput_tokensは617であった。gemini-3.1-flash-liteの一回目の出力と比較すると、1回目は項番を立てて回答があったのに対し、2回目は長めの文章をベースに回答していると感じた。