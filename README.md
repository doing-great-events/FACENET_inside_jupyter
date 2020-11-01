# Figure out the code line by line 逐行看懂FACENET
This ipynb file Run the FACENET totally inside the jupyter, use pre-trained weights from David Sandberg 
<br>本文檔使用 David Sandberg訓練好的參數, 全程於Jupyter介面執行FACENET
<br>
<br>Environments requirement 本文檔環境需求 : python 3.7, tensorflow 1.15, opencv 4.4
<br>will demo Real time face detect and dismantle into 4 step 動態即時偵測, 拆解成以下4步驟說明
<br><br>step1. Embedding photos into 512 vector by the facenet Incepton ResNet model, 
<br> and try to compare the L2 distane between different embedding
<br> 使用facenet Incepton ResNet v1 model將圖片轉譯成 512維的向量, 並且比較不同人臉產生的向量之L2 distance
<br><br>step2. extract face from dataset, and resize into 160 x 160 (requirement of facenet Incepton ResNet model)
<br> 使用MTCNN將照片中的人臉擷取出來, 並resize成 160 X 160 (作為facenet Incepton ResNet model的輸入)
<br><br>step3. train a classifier, we will identify the embedding face by this cliassifier
<br> 訓練classifier, 後續透過此classifier, 來辨識轉譯後的512維向量是誰的人臉
<br><br>step4. run the realtime face recognition
<br> 執行即時偵測辨識
 
# Code and pre-trained weights are mainly from David Sandberg All credit goes to David Sandberg
