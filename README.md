
# Project Title

Camera Intrinsic Parameter


## Index
### CPP TYPE
  - [Dependancy](#Dependancy) 
  - [Install](#Install)
  - [Parameter](#Parameter)
    - [Demo](#Demo)
  - [Results](#Results)
 - test
---
## CPP TYPE

### Dependancy

- ROS melodic ver
- Opencv 3.4 이상
- c++17

## Install

1. 직접세팅
```
** TODO
```

2. Docker 사용
 Docker 설치 및 Nvidia docker Image도 설치필요
```
$ sudo apt-get install x11-xserver-utils
$ xhost +

$ docker pull authorsoo/px4:9.0
$ docker run --gpus all -it --ipc=host  --expose 22 --net=host --privileged -e DISPLAY=unix$DISPLAY 
    -v /tmp/.X11-unix:/tmp/.X11-unix:rw -e NVIDIA_DRIVER_CAPABILITIES=all --name calib authorsoo/px4:9.0 bash

```

## Parameter
rosrun 이 아닌 launch 파일로 실행시길 경우 직접 파라미터 세팅
![launch file](https://user-images.githubusercontent.com/44966311/168318213-5733af5c-1723-4fea-98d8-90f480533510.png)
```
$ roslaunch mono_cam_calib mono_calib
```
## Demo
1. Dataset 이용
[Dataset](https://drive.google.com/a/tamu.edu/file/d/19Ke-oOhqkPKJBACmrfba4R5-w71_wrvT/view?usp=sharing)


도커 이용시 /home 디렉토리에 파일 존재함
```
$ rosrun mono_cam_calib mono_cam_calib
$ rosbag play [rosbag 파일명] // rosbag실행
```

[Demo Video](https://www.notion.so/superbai/Intrinsic-Calib-in-Gazebo-c4d0ac30e01f42908ce5e682d0faa9e9)

## Results
result폴더 Txt파일에 intrinsic, 왜곡, R, T 값들 

## TODO
파일 형식 txt 에서 Yaml 혹은 Json으로 변경

---
## PYTHON Type
** TODO





---

# MARKDOWN
MARKDOWN 정리, 실습 for README.md

# 1. 제목(글머리) 작성
# H1 제목  
## H2 부제목
### H3 소제목
#### H4 제목4
##### H5 제목5
###### H6 제목6


# 2. 번호 없는 리스트 작성
* 리스트1
  - 리스트2
    + 리스트3
    
# 3. 번호 있는 리스트 작성
1. 리스트1
2. 리스트2
3. 리스트3 

# 4. 이텔릭체(기울어진 글씨) 작성
*텍스트*

# 5. 굵은 글씨 작성
**텍스트**

# 6. 인용
> 인용1

> 인용2
>> 인용안의 인용

# 7. 수평선 넣기

---
  
# 8. 링크 달기
(1) 인라인 링크  

[블로그 주소](https://roboticsoo.shop)

(2) 참조 링크  

[블로그 주소][blog]

[blog]: https://jaehoon-daddy.tistory.com/

# 9. 이미지 추가하기
![이탈리아 포지타노](https://user-images.githubusercontent.com/31477658/85016059-f962aa80-b1a3-11ea-8c91-dacba2666b78.jpeg)

### 이미지 사이즈 조절
<img src="https://user-images.githubusercontent.com/31477658/85016059-f962aa80-b1a3-11ea-8c91-dacba2666b78.jpeg"  width="700" height="370">

### 이미지 파일로 추가하기
<img src="Capri_Island.jpeg" width="700">

# 10. 코드블럭 추가하기

```swift
public struct CGSize {
  public var width: CGFloat
  public var heigth: CGFloat
  ...
}
```

# etc

**텍스트 굵게**  
~~텍스트 취소선~~

### [개행]  

스페이스바를 통한 문장개행  
스페이스바를 통한 문장개행  

br태그를 사용한 문장개행
<br>
<br>
br태그를 사용한 문장개행


### [체크박스]

다음과 같이 체크박스를 표현 할 수 있습니다. 
* [x] 체크박스
* [ ] 빈 체크박스
* [ ] 빈 체크박스

### [이모지 넣기]
❤️💜💙🤍

### [표 넣기]
|왼쪽 정렬|가운데 정렬|오른쪽 정렬| 
|:---|:---:|---:| 
|내용1|내용2|내용3| 
|내용1|내용2|내용3| 

<br>
---

# Project Title

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

---
# Repository Quick Start template
## Index
  - [Overview](#overview) 
  - [Getting Started](#getting-started)
  - [Contributing](#contributing)
  - [Authors](#authors)
  - [License](#license)
<!--  Other options to write Readme
  - [Deployment](#deployment)
  - [Used or Referenced Projects](Used-or-Referenced-Projects)
-->
## About RepositoryTemplate
<!--Wirte one paragraph of project description -->  
This project's purpose is to create a make Repository with a collection of default settings  

## Overview
<!-- Write Overview about this project -->
**If you use this template, you can use this function**
- Issue Template
- Pull Request Template
- Commit Template
- Readme Template
- Contribute Template
- Pull Request Build Test(With Github Actions)

## Getting Started
**click `Use this template` and use this template!**
<!--
### Depencies
 Write about need to install the software and how to install them 
-->
### Installing
<!-- A step by step series of examples that tell you how to get a development 
env running

Say what the step will be

    Give the example

And repeat

    until finished
-->
1. Click `Use this template` button 
2. Create New Repository
3. Update Readme and Others(Other features are noted in comments.)
<!--
## Deployment
 Add additional notes about how to deploy this on a live system
 -->
## Contributing
<!-- Write the way to contribute -->
I am looking for someone to help with this project. Please advise and point out.  
Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code
of conduct, and the process for submitting pull requests to us.

## Authors
  - [Always0ne](https://github.com/Always0ne) - **SangIl Hwang** - <si8363@soongsil.ac.kr>

See also the list of [contributors](https://github.com/always0ne/readmeTemplate/contributors)
who participated in this project.
<!--
## Used or Referenced Projects
 - [referenced Project](project link) - **LICENSE** - little-bit introduce
-->

## License

```
MIT License

Copyright (c) 2020 always0ne

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

# Siesta

## Requirement

- Latest Node.js 14 LTS (recommend you to use [nvm](https://github.com/nvm-sh/nvm) or [asdf](https://github.com/asdf-vm/asdf))
- [Yarn 2](https://yarnpkg.com/getting-started/install#about-global-installs)

### Gentle Suggestions for Readings

- **[You know ask good questions](https://www.freecodecamp.org/news/how-to-ask-good-questions-as-a-developer-9f71ff809b63/). [한국어 비슷한 글](https://jbee.io/essay/good_questionor/)**
- [You are done react official tutorials](https://reactjs.org/docs/getting-started.html#learn-react)
- [You are done offical Next.js tutorials](https://nextjs.org/learn/basics/create-nextjs-app)
- [You are good at TypeScript](https://www.typescriptlang.org/docs/handbook/intro.html)
- [You know concepts of Yarn 2](https://yarnpkg.com/features/pnp)
- [We use Stitches to style our application](https://stitches.dev/docs/introduction)
- [We prefer flat folders and long file name](https://twitter.com/dan_abramov/status/1145354949871767552?lang=en)

## Installation

```sh
$ yarn
```

## Development

```sh
$ yarn dev

# upgrade deps with interactive CUI
$ yarn upgrade-interactive

# update yarn version for this project
$ yarn set version latest
```

### Structure

```sh
.
├── jest            # Jest Configurations
├── cypress         # Cypress configurations & tests
├── src
│   ├── apis        # API Fetch functions
│   ├── assets      # Static resources that will be transpiled
│   ├── components  # React components
│   ├── hooks       # React custom hooks
│   ├── itly        # Auto-generated tracking code, see below
│   ├── misc        # Ambiguous little things
│   ├── modes       # Mold Modes
│   ├── pages       # Next.js pages
│   ├── shapes      # Mold Shapes
│   ├── shared      # Core Utility / Interface
└───└── stitches    # Stitches Definition
```

### Itly (Amplitude)

The contents of `itly/` are auto-generated by the Amplitude Data CLI (Iteratively).

To update the tracking plan, run [`ampli pull`](https://developers.data.amplitude.com/using-the-ampli-cli/). [Find more information in Notion](https://www.notion.so/superbai/User-event-tracking-78dcf8a169ad4d5f9d862ccfb651ca0c)

## Productivity

- [We avoid hasty abstraction](https://kentcdodds.com/blog/aha-programming)
- [Duplication doesn't matter](https://overreacted.io/the-wet-codebase/)
- [We write test code to save our times and make more value](https://testingjavascript.com/)
- [Recommend you to read all test posts of Kent](https://kentcdodds.com/blog?q=test)
- [Don't Solve Problems, Eliminate Them](https://kentcdodds.com/blog/don-t-solve-problems-eliminate-them)

## Deployment

We use [Vercel](https://vercel.com/docs) to deploy [our project](https://vercel.com/superb-ai/siesta).

- `main` branch deployed as production: https://suite-anno-v2.superb-ai.com
- `stage` branch deployed as QA preview (almost same as production): https://stage.suite-anno-v2.superb-ai.com
- `develop` branch deployed as preview: https://dev.suite-anno-v2.superb-ai.com
- other branches deployed as preview

## Other Recommendations

- [Thinking in GraphQL](https://relay.dev/docs/principles-and-architecture/thinking-in-graphql/)
- [Thinking in Relay](https://relay.dev/docs/principles-and-architecture/thinking-in-relay/)
- [React Design Principals](https://reactjs.org/docs/design-principles.html)


<!-- <div align="center">
  <img src="resources/mmdet3d-logo.png" width="600"/>
  <div>&nbsp;</div>
  <div align="center">
    <b><font size="5">OpenMMLab website</font></b>
    <sup>
      <a href="https://openmmlab.com">
        <i><font size="4">HOT</font></i>
      </a>
    </sup>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <b><font size="5">OpenMMLab platform</font></b>
    <sup>
      <a href="https://platform.openmmlab.com">
        <i><font size="4">TRY IT OUT</font></i>
      </a>
    </sup>
  </div>
  <div>&nbsp;</div>
</div> -->


<!-- --- -->

## Install

- set env
```
$ docker build -t mmdetection3d -f docker/Dockerfile .
```

## Set Data

### 1. Kitti Data
Download KITTI 3D detection data [Here](http://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d). Prepare KITTI data splits by running
```
mkdir ./data/kitti/ && mkdir ./data/kitti/ImageSets

# Download data split
wget -c  https://raw.githubusercontent.com/traveller59/second.pytorch/master/second/data/ImageSets/test.txt --no-check-certificate --content-disposition -O ./data/kitti/ImageSets/test.txt
wget -c  https://raw.githubusercontent.com/traveller59/second.pytorch/master/second/data/ImageSets/train.txt --no-check-certificate --content-disposition -O ./data/kitti/ImageSets/train.txt
wget -c  https://raw.githubusercontent.com/traveller59/second.pytorch/master/second/data/ImageSets/val.txt --no-check-certificate --content-disposition -O ./data/kitti/ImageSets/val.txt
wget -c  https://raw.githubusercontent.com/traveller59/second.pytorch/master/second/data/ImageSets/trainval.txt --no-check-certificate --content-disposition -O ./data/kitti/ImageSets/trainval.txt
```
Generate info file
```
python tools/create_data.py kitti --root-path ./data/kitti --out-dir ./data/kitti --extra-tag kitti
```
### 2. Suite Data
- Convert Suite to Kitti Data Format

  reference  : custom_data.ipynb in https://github.com/Superb-AI-Suite/voda.git
  
  [TODO] Make a script to download asset / label from suite project with login information.

- Debug : Kitti_GT_3Dbbox_visualization.ipynb in https://github.com/Superb-AI-Suite/voda.git

- Generate info file
```
python tools/create_data.py kitti --root-path ./data/superb --out-dir ./data/superb --extra-tag kitti
```

## Demo
### 1. kitti
```
python tool/train.py configs/configs/parta2/hv_PartA2_secfpn_2x8_cyclic_80e_kitti-3d-car.py
```

### 2. Suite
```
python tool/train.py configs/configs/superb/custom.py
```
or Using **train_demo.ipnb**

## Main Config
- reference : **/config/superb/custom.py**
- dataset_type : select in [Kitti, cityspace, waymo, nuscenes], Our code based on Kitti
- data_root = 'data/superb/', custom data(suite -> kitti)
- point_cloud_range : velodyne coordinates, x, y, z
- input_modality : use_lidar=True, use_camera=False
- resume_from : load pretrained model
- checkpoint_config = set interval of saving  checkpoint and path

  ex) dict(interval=3, out_dir='/home/eunsoo/dl/mmdetection3d/checkpoints/')

- evaluation : set evalutation metric

  ex)  cfg.evaluation.metric = ['bbox', 'segm']

- learning rate, batch size

  ex)  cfg.optimizer = dict(type='SGD', lr=0.0025, momentum=0.9, weight_decay=0.0001)

**Error Situation**
1. Nothing PCD in BBox bbox
2. Out of range when appling data augmentation
