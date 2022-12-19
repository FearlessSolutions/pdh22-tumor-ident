# Identifying Brain Tumors in MRI Scans

## Purple Data Hacks '22

Purple Data Hacks (PDH) is a hackathon where Fearless invests in developing its
internal data capabilities. In 2022, PDH'22 was a two day event taking place on
December 15th, 2022 from 08:00 -- 16:00, to December 16th, 2022 from 08:00 --
16:00. The event was hybrid, with 20% of participants participating in a fully
remote capacity. This event was facilitated by 
[Nick Saccente](https://github.com/nsaccente)

## Challenge

* **Data Format**: 7023 images of MRI images

* **Problem Domains**: Computer Vision, Classification, Supervised Learning

* **Portfolio/Agency**: CMS, Health & Sciences Portfolio

A tumor is a mass of abnormal cells that can grow indefinitely. Since the human
skull is rigid, a tumor of the brain may cause increased pressure in the
cranium that can lead to seizures, brain damage, or death. Identifying brain
tumors while they are still operable can save lives. CMS wants to incorporate
automated tumor detection to reduce the costs and fatalities associated with
catching a tumor in later stages.

## Solution
My solution was a model that was transfer learned on EfficientNetB0 to that
achieved the following:
```
              precision    recall  f1-score   support

           0       0.79      0.99      0.88       127
           1       0.98      0.79      0.87       141
           2       0.98      0.98      0.98       162
           3       0.99      0.96      0.97       142

    accuracy                           0.93       572
   macro avg       0.94      0.93      0.93       572
weighted avg       0.94      0.93      0.93       572


where:
0 = Glioma Tumor
1 = No Tumor
2 = Meningioma Tumor
3 = Pituitary Tumor
```


The dataset used to train this model can be found
[here](https://drive.google.com/file/d/1MJ0k0f4ODFfSxrVlToxXC6VKf5oNkRUs/view?usp=sharing)
