# LandmarkRetireval
Development of Landmark Retrieval System for Video Based on Deep Learning

# Development of Landmark Retrieval System for Video Based on Deep Learning

## Get started
1. Download the data files 'train.csv' (landmark data-set including 44 classes)
2. Set up environment. (refer to 'environment_landmark007.yml')
3. Move on to the codes.


## Codes
### Landmark Recognition Model
The script '**download**' consists of the code to
1. Download resized images
2. Move the images into folders labelled by class name
3. Some visualizations

The script '**train**' consists of the code to Transfer Learning using Keras.

### Web
The script '**app**' consists of the code to **Upload** and **Search** videos.

The script '**predictNew**' consists of the code to predict on test images(video scenes).

The script '**delfNew**' consists of the code used for image retrieval done by matching local features.

The script '**dbNew**' consists of the code to
1. Store data in the database.
2. Copy scene images to ../web/static.
3. Delete some files to reset folder.


## Folder Structure
The folder '**data**' consists of
1. Images to train, validate, and test the model
2. CSV files of the landmark dataset

The folder '**script**' consists of the scripts.

The folder '**web**' consists of
1. Scripts to run web application.
2. Database
3. Videos and images


/*기존의 비디오 검색 서비스는 비디오의 제목, 설명, 해시태그 등 텍스트 기반 검색을 사용한다. 
비디오의 길이가 길수록 텍스트만으로는 전체 내용을 표현하기 어려워 정확한 검색에 한계가 있다. 
본 프로젝트에서는 비디오 내용을 고려한 검색이 가능하도록 딥러닝 기반의 비디오 내 공간정보 검색 시스템을 제안한다. 
비디오의 장면 전환 구간마다 어떤 공간인지를 판단함으로써 공간 키워드를 통한 검색이 가능하다. 
비디오에서 모든 장면 이미지를 추출한 뒤, 훈련된 랜드마크 인식 모델로 장면 이미지에 대하여 클래스를 예측한다. 
예측된 클래스의 이미지 셋과 장면 이미지를 비교함으로써 결과가 올바른지 검증한다. 
실험을 위해 학습 데이터 7,222장과 실험 데이터 1,769장의 랜드마크 이미지 데이터 셋을 구축하였다. 
실험 결과에 따르면 86.67%의 정확도로 이미지에서 랜드마크를 인식할 수 있었다. 
또한 DeLF 모듈을 사용하여 인식 결과를 검증하여 정확도를 개선한다. */
