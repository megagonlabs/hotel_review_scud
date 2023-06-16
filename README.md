
# Hotel Review SCUD and dialogs

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a>
[![CI](https://github.com/megagonlabs/hotel_review_scud/actions/workflows/ci.yml/badge.svg)](https://github.com/megagonlabs/hotel_review_scud/actions/workflows/ci.yml)
[![Typos](https://github.com/megagonlabs/hotel_review_scud/actions/workflows/typos.yml/badge.svg)](https://github.com/megagonlabs/hotel_review_scud/actions/workflows/typos.yml)

## Overview

### SCUDs for reviews

| Item | Content |
| --- | --- |
| Review |平和記念公園へも徒歩圏内で駐車場もあり、便利なホテルです。 |
| SCUD | 平和記念公園が▔ホテルから▔徒歩圏内だ。<br>駐車場が▔ホテルに▔ある。<br>ホテルが▔便利だ。 |

- Data: ``data/vanilla/jalan/jalan.VanillaUtterance.jsonl``
    - A part of [hotel reviews](https://github.com/megagonlabs/ebe-dataset)
- SCUD: ``data/scud/jalan/jalan_scud_long.Example.jsonl``
    - Phrases are separated by ``▔``(U+2594)
    - ``meta["exphora"]``
        - ``true`` if it is necessary to refer to a sentence other than the target sentence for SCUD generation, else ``false``
- SCUD correctness annotation: ``data/correctness_labeled_scud/jalan/jalan.Example.jsonl``

### \[Bonus\] Accommodation search dialogs by using reviews (3,413 examples)

- Data: ``data/vanilla/dialog/5turn.ebe.VanillaUtterance.jsonl``
    - Japanese dialogs between a customer and an operator in a fictitious accommodation consultation service
    - Each dialog ends with ``それでは、『〜〜』とレビューにある、こちらの宿はいかがでしょうか?``
    - Each recommendation and recommended hotel is selected from [hotel reviews](https://github.com/megagonlabs/ebe-dataset)

    | Name | Utterance |
    | --- | --- |
    | agent | チェックアウトされてからのご予定はありますか? |
    | user | 特にありません。最終日も、なるべく長い時間ホテルで過ごしたいです。|
    | agent | それでは、チェックアウト時間が遅いほうがよろしいですか? |
    | user | そうですね、その条件で探して頂けますか? |
    | agent | それでは、「16時チェックアウトでゆっくり出来ました。」とレビューにある、こちらの宿はいかがでしょうか? |

## Format

Formats of all files in [data](data) are the same as used in [asdc](https://github.com/megagonlabs/asdc).

## References

1. 林部祐太．
    発話とレビューに対する解釈文生成とトピック分類．
    言語処理学会第29回年次大会論文集，pp.2013-2017. 2022. (NLP 2022)
    [\[PDF\]](https://www.anlp.jp/proceedings/annual_meeting/2023/pdf_dir/P8-12.pdf)

## Notes

- 株式会社リクルート（以下「リクルート」といいます。）は自然言語処理の研究に貢献する目的で、言語的注釈が付与されたデータセット（以下「本データセット」といいます。）を公開いたします。
- Recruit Co., Ltd.(hereinafter referred to as "Recruit") publishes the data set with linguistic annotations (hereinafter referred to as this "Data Set") for the purpose of contributing to the study of natural language processing.

- 本データセットには、レビューデータから抽出した文、それらを加工した文、アノテーション作業者が付与した判定ラベルが含まれます。ラベルは作業者によって付与されたものであり、クチコミ投稿者の体験や評価、もしくはリクルートの評価を反映したものではありません。
- This Data Set is constructed using various methods of extraction from Customer Reviews. Annotators provide judgment via labels. Labels and recommendation sentences are provided by the cloud-sourced annotators and do not reflect the experience, assessment, or Recruit’s assessment of the review contributor.

- 事実と異なる内容が含まれる場合があります。
- This Data Set may contain content that is contrary to the facts.

- 本データセットは通知なく変更・削除される場合があります。
- This Data Set is subject to change or deletion without notice.

## License and Attribution

- 本データセットに含まれる「じゃらんレビューデータ」の著作権は、リクルートに帰属します。
- The copyrights to Customer Reviews included in this Data Set belong to Recruit.

- 本データセットを用いた研究発表を行う際は、[References](#references)の論文を引用し、次のようにデータの入手元も記述してください。
    - 文例： 本研究では株式会社リクルートが提供するxxxxを利用しました。
- When publishing a study using this dataset, please cite papers in [References](#references) and describe the source of the data as follows.
    - Example: To conduct this study, we used xxxx provided by Recruit Co., Ltd.

- 本データセットのライセンスは[クリエイティブ・コモンズ・ライセンス (表示-非営利-継承 4.0 国際)](https://creativecommons.org/licenses/by-nc-sa/4.0/)です。
- The license of this Data Set is in the same scope as [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Prohibitions

- リクルートは本データセットを非営利的な公共利用のために公開しています。分析・研究・その成果を発表するために必要な範囲を超えて利用すること（営利目的利用）は固く禁じます。
- Recruit discloses this Data Set for non-profit public use. It is strictly prohibited to use for profit purposes beyond the scope necessary for the presentation of analysis, research and results.

- 利用者は、研究成果の公表といえども、前項の出版物等の資料に、適正な例示の範囲を超えてデータセット中のデータを掲載してはならず、犯罪その他の違法行為を積極的に助長・推奨する内容や公序良俗に違反する情報等を記述しないでください。
- Even when publishing research results, users should not post data in the data set beyond the appropriate exemplary range in the publications and other materials set forth in the preceding paragraph. Users should not describe information obtained from the data set that violates public order and morals, promote or encourage criminal or other illegal acts.

## Contact

If you have any inquiries and/or problems about a dataset or notice a mistake, please contact NLP Data Support Team ``nlp_data_support at r.recruit.co.jp``.
