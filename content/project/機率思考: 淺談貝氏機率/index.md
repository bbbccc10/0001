---
title: 機率思考
summary: 貝葉斯推理的一個例子
tags:
  - ML
date: 2022-01-01
external_link: http://github.com
---

貝葉斯統計是一種將概率應用於統計問題的數學過程。 它為人們提供了更新他們對來自新數據的證據的信念的工具[^1]。

貝葉斯方法是準確地寫下概率（首先是先驗可能性 --> 可能事件的特異性和敏感性的條件可能性 --> 後驗可能性，我們可以總結出真陽性和假陰性可能性）。 我們想根據我們已知的數據進行推斷，並直接求解得到的方程——這迫使我們明確地處理所有可能出現的數學困難、額外的假設和不確定性。

P 值稱為概率值。 它被定義為獲得與實際觀察結果相同或更極端的結果的概率。如：
(1) P-value > 0.05，結果無統計學意義，不拒絕原假設。[^2]
(2) P-value < 0.05，結果具有統計學意義。 通常，拒絕原假設而支持備擇假設。[^2]
(3) P-value < 0.01，結果具有高度統計顯著性，從而拒絕原假設，支持備擇假設。[^2]

貝葉斯方法允許通過將 p 值轉換為針對零假設 (H) 的證據的直接度量來校準 p 值，即所謂的貝葉斯因子[^1]。

貝葉斯因子是一個特定假設的可能性與另一個假設的可能性之比。 它可以解釋為衡量支持兩個相互競爭的假設中的一個理論的證據強度。

如果貝葉斯因子大於 1，則後驗概率將大於先驗概率，因此零假設 (H) 的後驗概率將大於其先驗概率[^4]。 相反，如果零假設小於 <1，則零假設的後驗概率小於先驗概率。 因此，貝葉斯因子表示數據中的證據如何修改先驗概率[^4]。

貝葉斯因子為我們提供了數學工具，可以根據看到有關這些事件的新數據或證據來更新我們對隨機事件的信念，這使得它對科學、政治和商業領域很重要。 貝葉斯推理將概率解釋為個人對特定事件的發生可能擁有的可信度或信心的度量。 貝葉斯統計能夠給出兩個假設（原假設和備擇假設）的概率分佈。 它們還允許以後驗分佈的形式向假設添加新信息。 重要的是要注意遇到的一些困難是（1）它是計算密集型的[^3] ，（2）貝葉斯方法需要指定先驗概率分佈，這些分佈本身通常是未知的[^3] 


[^1] Anesi, Chuck. Kahneman's Example of Elementary Bayesian Inference from Thinking Fast and Slow, https://www.anesi.com/bayes.htm. 
[^2] Beers, Brian. “P-Value: What It Is, How to Calculate It, and Why It Matters.” Investopedia, Investopedia, 15 Dec. 2022, https://www.investopedia.com/terms/p/p-value.asp#:~:text=Is%20a%200.05%20p-value,null%20hypothesis%20is%20not%20rejected. 
[^3] Eddy, Sean R. “What Is Bayesian Statistics?” Nature Biotechnology, vol. 22, no. 9, 2004, pp. 1177–1178., https://doi.org/10.1038/nbt0904-1177. 
[^4] Nss. “Bayesian Statistics Explained in Simple English for Beginners.” Analytics Vidhya, 2 Dec. 2022, https://www.analyticsvidhya.com/blog/2016/06/bayesian-statistics-beginners-simple-english/#h2_4. 
