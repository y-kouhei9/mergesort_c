# mergesort_c

### 概要

マージソートのアルゴリズム  
C言語による実装

### 説明

1. マージとは  
	統合すること  
	1. 整列済の二つの配列AとBを空の配列Cに統合する  
		1. 用意するもの  
			1. 配列Aの先頭の要素を示すポインタi
			1. 配列Bの先頭の要素を示すポインタj
			1. 配列Cの先頭の要素を示すポインタk
		1. 手順  
			1. ポインタiとjを比較する
			1. 比較した結果、小さい値をポインタkに格納する
			1. 小さい値を指しているポインタ(iもしくはj)を一つ進める
			1. ポインタkを一つ進める
			1. この動作を繰り返す
			1. もしどちらかのポインタが配列の最後に達し、配列の最後を超えた場合、  
				もう一方の配列のポインタの現在位置から配列の最後までの値を  
				そのままkに代入していく(代入されるたび、ポインタkは+1される)

	1. 計算量  
		統合する二つの配列の大きさを、それぞれmとnとした時、  
		O(m+n)  

	1. 一つの配列でマージを行うには  
		1. 用意するもの  
			1. 前後にソート済の配列をもつ配列A
			1. 配列Aの前部分のソート済配列の先頭の要素を示すポインタi
			1. 配列Aの後ろ部分のソート済配列の先頭の要素を示すポインタj
			1. 配列Aの先頭の要素を示すポインタl
			1. 配列Aの最後の要素を示すポインタh
			1. 配列Aの中央の要素を示すポインタmid
			1. 同じ大きさの配列B
			1. 配列Bの先頭の要素を示すポインタk
		1. 手順  
			1. iとjを比較し、小さい方を配列Bの先頭から格納する
			1. 小さい方のポインタを+1する
			1. 配列Bを配列Aにコピーする

	1. 複数の配列でマージを行う  
		複数の配列でマージを行う(M-way merging)には、  
		配列の個数分のポインタを用意する。それぞれのポインタは  
		それぞれの配列の先頭の要素を指し示す。ポインタが指している  
		要素だけで配列を作成し、その中で一番小さい値を別の配列に格納する。  
		その後、該当した一番小さい値を指し示したポインタを+1し、繰り返す。  
		複数の配列をマージする際は、一度に全ての配列をマージするのではなく、  
		徐々に大きな配列にしていく。

1. Iterative(反復)なマージソート  
	配列の各要素を隣同士でマージしていく    
	処理時間はO(nlogn)  

1. Recursive(再帰的)なマージソート  
	

