# 2D-Object-Detection-leaderboard
2D Object Detection leaderboard


<p><img src="https://camo.githubusercontent.com/8858f8b1c9fb4847f25610527af88d2b3abde054/68747470733a2f2f757365722d696d616765732e67697468756275736572636f6e74656e742e636f6d2f32363833333433332f3132373537343938382d36613535386161312d643236382d343462392d626636622d3632643463363035636337322e6a7067" alt="" width="640" height="360" /></p><p>&nbsp;</p>


# Overview


<p>본 챌린지는 '2D Object Detection'을 수행하는 챌린지입니다. 2D Object Detection은 2D 영상 내에서 특정 클래스의 개체 인스턴스를 검색하는 작업입니다. 해당 기술은 크게 One-stage method와 Two-stage method로 분류할 수 있습니다. One-stage method는 추론 속도를 우선시하며, 대표적으로는 YOLO, SSD 및 RetinaNet이 포함됩니다. Two-stage method는 검출 정확도를 우선시하며, 대표적으로는 Faster R-CNN, Mask R-CNN, 그리고 Cascade R-CNN이 있습니다. 본 챌린지에서는 One-stage method로 한정하며, 해당 method의 가장 대표적인 모델중 하나인 YOLO을 베이스라인으로 선정하였습니다.</p>
<ul>
<li>베이스라인 방법론: YOLOv5</li>
<li>베이스라인 코드: <a href="https://github.com/ultralytics/yolov5/">https://github.com/ultralytics/yolov5</a></li>
</ul>
<p>&nbsp;</p>
<ul>
<li>평가대상:(YOLOv5x 모델)</li>
<li>tutorial 노트북 제공됨(<a href="https://github.com/ultralytics/yolov5/blob/master/tutorial.ipynb">링크</a>)</li>
</ul>
<p>&nbsp;</p>

<ul>
<li>챌린지 설명 동영상 </li>
<li>(<a href="https://youtu.be/V1lnjEATIlU">링크</a>)</li>
</ul>
<p>&nbsp;</p>

<ul>
<li>베이스라인 논문 </li>
<li>(<a href="https://pjreddie.com/media/files/papers/yolo_1.pdf">링크</a>)</li>
</ul>
<p>&nbsp;</p>

<ul>
<li>베이스라인 논문 발표 영상 </li>
<li>(<a href="https://www.youtube.com/watch?v=NM6lrxy0bxs">링크</a>)</li>
</ul>
<p>&nbsp;</p>


# Dataset

<ul>
<li>데이터 셋: MS COCO(<a href="https://cocodataset.org/#download">링크</a>)</li>
<li>2017 Train/val image 및 annotation 이용</li>
<li>Test set의 annotation이 제공되지 않으므로, Validation set을 이용해 평가합니다.</li>
<li>Train set을 분할하여 검증에 이용하시기 바랍니다.</li>
</ul>
<p>&nbsp;</p><p>&nbsp;</p>



# Evaluation


<p>해당 챌린지의 평가 지표는 mAP (mean Average Precision)입니다.</p>
<p>해당 지표의 대한 설명은 <a href="https://cocodataset.org/#detection-eval">(링크)</a> 에서 확인할 수 있습니다.</p>
<p>본 챌린지에서는 mAP% AP at IoU=.50:.05:.95 (primary challenge metric)을 이용합니다.</p>
<p>&nbsp;</p><p>&nbsp;</p>



# Submission


<p>본 챌린지의 결과 제출은 MS COCO dataset의 test set의 annotation이 제공되지 않으므로, validation set을 이용합니다.</p>
<p>제출 형식은 json 파일로 제출가능하며, 아래 형식에 맞춰 제출하시기 바랍니다. <a href="https://cocodataset.org/#format-results">(참조)</a> <a href="https://github.com/cocodataset/cocoapi/blob/master/results/instances_val2014_fakebbox100_results.json">(참조2)</a></p>
<pre>[{
"image_id": int, "category_id": int, "bbox": [x,y,width,height], "score": float,
}]</pre>
<p>&nbsp;</p><p>&nbsp;</p>

# 3단계 추천 논문
<p>추천 논문은 2021 CVPR 2D Object Detection 분야 논문중 코드가 공개되지 않은 논문들로 선정하였습니다.</p>
<ul>
<li>Joint-DetNas </li>
<li>(<a href="https://openaccess.thecvf.com/content/CVPR2021/papers/Yao_Joint-DetNAS_Upgrade_Your_Detector_With_NAS_Pruning_and_Dynamic_Distillation_CVPR_2021_paper.pdf">링크</a>)</li>
</ul>

<ul>
<li>IQDet </li>
<li>(<a href="https://openaccess.thecvf.com/content/CVPR2021/papers/Ma_IQDet_Instance-Wise_Quality_Distribution_Sampling_for_Object_Detection_CVPR_2021_paper.pdf">링크</a>)</li>
</ul>

<ul>
<li>RankDetNet </li>
<li>(<a href="https://openaccess.thecvf.com/content/CVPR2021/papers/Liu_RankDetNet_Delving_Into_Ranking_Constraints_for_Object_Detection_CVPR_2021_paper.pdf">링크</a>)</li>
</ul>

