---
title: "Basic_mathematics"
date: 2018-12-14T10:59:42+09:00
draft: false
---

# 「AI」エンジニアになるための「基礎数学」再入門のメモ

<http://www.atmarkit.co.jp/ait/series/11405/>

## 01

<http://www.atmarkit.co.jp/ait/articles/1810/10/news009.html>

### 「AI人材」

<table>
    <tr>
        <th>大区分</th>
        <th>小区分</th>
        <th>やること</th>
    </tr>
    <tr>
        <td rowspan="2">AI人材</td>
        <td>AIビジネスマン</td>
        <td>AIプロジェクトに関する意思決定</td>
    </tr>
    <tr>
        <td>AIエンジニア</td>
        <td>AIを開発。AIの精度向上</td>
    </tr>
</table>

この講座はITエンジニアをAIエンジニアの土俵にあげる。そのための「数学」

## 02

<http://www.atmarkit.co.jp/ait/articles/1810/10/news009.html>

### 測定

データの分類

<table>
    <tr>
        <th>大分類</th>
        <th>中分類</th>
        <th>中分類-説明</th>
        <th>小分類</th>
        <th>小分類-説明</th>
        <th>足し算・引き算</th>
        <th>掛け算・割り算</th>
        <th>値のカウント</th>
        <th>最頻値</th>
        <th>中央値</th>
        <th>平均値</th>
        <th>幾何平均値</th>
    </tr>
    <tr>
        <td rowspan="4">データ</td>
        <td rowspan="2">質的データ</td>
        <td rowspan="2">分類や種別を判別する値。計算の結果に意味がない。文字であることが多い。</td>
        <td>名義尺度</td>
        <td>
            <ul>
                <li>男性/女性、赤色/青色など。女性1、男性を2としてとき、1+2（男性+女性）に意味はない</li>
                <li>同様に平均値や中央値にも意味はない</li>
                <li>ただし、最頻値には意味がある。</li>
            </ul>
        </td>
        <td>×</td>
        <td>×</td>
        <td>○</td>
        <td>○</td>
        <td>×</td>
        <td>×</td>
        <td>×</td>
    </tr>
    <tr>
        <td>順序尺度</td>
        <td>
            <ul>
                <li>「0:嫌い、1:普通、2:好き」のようなデータ</li>
                <li>2-1（好き - 普通）も、1-0（普通-嫌い）も、共に1だが同じと扱ってはいけない。</li>
                <li>順序尺度には「等間隔性」がない。普通と好きは近いが、普通と嫌いの左は大きいかもしれない。</li>
            </ul>
        </td>
        <td>×</td>
        <td>×</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>×</td>
        <td>×</td>
    </tr>
    <tr>
        <td rowspan="2">量的データ</td>
        <td rowspan="2">数字として意味があり、計算できる。</td>
        <td>間隔尺度</td>
        <td>
            <ul>
                <li>気温（℃）　27℃、28℃など</li>
                <li>「等間隔性」はあるが「0が何もない状態ではない」ので注意が必要</li>
                <li>0℃は273K</li>
                <li>27℃を2倍すると54℃。ただし、300Kが327Kになっただけ</li>
                <li>足し算引き算は出来るが、掛け算、割り算に意味がない。</li>
            </ul>
        </td>
        <td>○</td>
        <td>×</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>×</td>
    </tr>
    <tr>
        <td>比尺度</td>
        <td>「等間隔性」があり「0が何もない状態」のもの。絶対零度、売上や利益、行動回数（アクセス回数、ログイン回数、購入回数）
        </td>
                <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
        <td>○</td>
    </tr>
</table>


