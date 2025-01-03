## Paper review index for Test-time Training/Learning

| Index                                                                                             | Title & Link                                                                                                                                                                                                                                                                                                     | Paper                                                                                                                                   | Submission | Year |
| ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---- |
| [[01. Test-time training with self-supervision for generalization under distribution shifts\|01]] | [**Test**-**time training** with **self**-**supervision** for generalization under distribution shifts](http://proceedings.mlr.press/v119/sun20b.html)                                                                                                                                                           | [[learning_methods/test_time/paper/01. Test-time training with self-supervision for generalization under distribution shifts.pdf\|pdf]] | #PMIR      | 2020 |
| [[02. Test-time training for out-of-distribution generalization\|02]]                             | [**Test**-**time training** for out-of-distribution generalization](https://openreview.net/forum?id=HyezmlBKwr)                                                                                                                                                                                                  | [[learning_methods/test_time/paper/02. Test-Time Training for Out-of-Distribution Generalization.pdf\|pdf]]                             | #ICLR      | 2019 |
| [[03. Test-time training with masked autoencoders\|03]]                                           | [**Test**-**time training** with masked autoencoders](https://proceedings.neurips.cc/paper_files/paper/2022/hash/bcdec1c2d60f94a93b6e36f937aa0530-Abstract-Conference.html)                                                                                                                                      | [[learning_methods/test_time/paper/03. Test-Time Training with Masked Autoencoders.pdf\|pdf]]                                           | #NeurIPS   | 2022 |
| 04                                                                                                | [Fully **Test-time Adaptation** for **Object Detection**](https://openaccess.thecvf.com/content/CVPR2024W/MAT/html/Ruan_Fully_Test-time_Adaptation_for_Object_Detection_CVPRW_2024_paper.html)                                                                                                                   | [[04. Fully Test-time Adaptation for Object Detection.pdf\|pdf]]                                                                        | #CVPR      | 2024 |
| 05                                                                                                | [MonoTTA: Fully **test-time adaptation** for Monocular 3D **Object Detection**](https://link.springer.com/chapter/10.1007/978-3-031-72784-9_6)                                                                                                                                                                   | [[05. Monotta - Fully test-time adaptation for monocular 3d object detection.pdf\|pdf]]                                                 | #EECV      | 2024 |
| 06                                                                                                | [Ev-TTA: **Test**-**time adaptation** for event-based **object recognition**](http://openaccess.thecvf.com/content/CVPR2022/html/Kim_Ev-TTA_Test-Time_Adaptation_for_Event-Based_Object_Recognition_CVPR_2022_paper.html)                                                                                        | [[06. Ev-tta - Test-time adaptation for event-based object recognition.pdf\|pdf]]                                                       | #CVPR      | 2022 |
| 07                                                                                                | [**Test time adaptation** with regularized loss for weakly supervised salient **object detection**](http://openaccess.thecvf.com/content/CVPR2023/html/Veksler_Test_Time_Adaptation_With_Regularized_Loss_for_Weakly_Supervised_Salient_CVPR_2023_paper.html)                                                    | [[07. Test Time Adaptation With Regularized Loss for Weakly Supervised Salient Object Detection.pdf\|pdf]]                              | #CVPR      | 2023 |
| 08                                                                                                | [Weakly Supervised **Test**-**Time** Domain **Adaptation** for **Object Detection**](https://arxiv.org/abs/2407.05607)                                                                                                                                                                                           | [[08. Weakly Supervised Test-Time Domain Adaptation for Object Detection.pdf\|pdf]]                                                     | #Pre-Print | 2024 |
| 09                                                                                                | [Contrastive **Test**-**Time Adaptation**](http://openaccess.thecvf.com/content/CVPR2022/html/Chen_Contrastive_Test-Time_Adaptation_CVPR_2022_paper.html)                                                                                                                                                        | [[09. Contrastive Test-Time Adaptation.pdf\|pdf]]                                                                                       | #CVPR      | 2022 |
| 10                                                                                                | [Improved **Test**-**Time Adaptation** for Domain Generalization](http://openaccess.thecvf.com/content/CVPR2023/html/Chen_Improved_Test-Time_Adaptation_for_Domain_Generalization_CVPR_2023_paper.html)                                                                                                          | [[10. Improved Test-Time Adaptation for Domain Generalization.pdf\|pdf]]                                                                | #CVPR      | 2023 |
| 11                                                                                                | [A Comprehensive Survey on **Test-Time Adaptation** Under Distribution Shifts](https://idp.springer.com/authorize/casa?redirect_uri=https://link.springer.com/article/10.1007/s11263-024-02181-w&casa_token=Ty5gxDeYNYoAAAAA:92SNqYPDGizZR_EDQikzmv5Bml51NhvQxmZeUEE_rXxG1DOgB_OK9j5wUaA3pxwokSQwDPhEa5XdR2kqXQ) | [[11. A Comprehensive Survey on Test-Time Adaptation Under Distribution Shifts.pdf\|pdf]]                                               | #IJCV      | 2024 |
|                                                                                                   |                                                                                                                                                                                                                                                                                                                  |                                                                                                                                         |            |      |

#### 발전사

##### 개요
- Domain Adaptation 분야는 모델이 학습된 도메인(Source Domain)과 다른 도메인(Target Domain)에서도 잘 작동하도록 돕는 기술을 연구하는 분야로, 데이터 분포의 변화에 적응하는 과정을 포함한다. 이 분야는 여러 하위 개념과 방법론을 통해 발전해왔으며, 특히 UDA(Unsupervised Domain Adaptation), SFDA(Source-Free Domain Adaptation), TTA(Test-Time Adaptation), 그리고 TTT(Test-Time Training)로 점진적으로 확장되었다.
- Domain Adaptation의 하위 분야(UDA, SFDA)는 도메인 차이를 줄이고 Target Domain에서의 성능을 높이는 데 중점을 둔다. 그러나 **라벨 의존성 부족, 복잡한 Distribution Shift, Generalization 한계, 데이터 품질 의존성 등의 공통된 한계**를 가진다. FTTA는 TTA의 확장된 형태로, Test 단계에서 완전한 자율성을 가지고 모델을 지속적으로 학습시키는 접근법이다.
- Domain Adaptation은 라벨 전이의 필요성을 줄이며, 점진적으로 Source 데이터에 대한 의존성을 없애고, Target 데이터에 실시간으로 적응하는 방향으로 발전했다. 초기 UDA는 Source 데이터를 기반으로 Target Domain에 적응했으나, SFDA로 넘어가면서 **Source 데이터 접근을 제거**하고 Target 데이터에만 집중했다. 이후 TTA는 **Test 단계에서 실시간 적응**을 가능하게 하였으며, 최종적으로 TTT는 실시간 적응뿐만 아니라 **추가 학습을 통해 지속적으로 모델을 개선**하는 방식으로 진화했다.

##### 구분

###### **1. Domain Adaptation (DA)**
- **특징**: Source Domain 데이터를 활용해 Target Domain에서의 성능을 개선.
- **한계**: Source와 Target 간의 분포 차이가 클 경우 성능 저하.
- 핵심 논문: "Domain-Adversarial Training of Neural Networks (DANN)" - Ganin et al. (2016)
	- 핵심: Adversarial Training을 이용해 Feature Space에서 도메인 불변성을 학습.
###### **2. Unsupervised Domain Adaptation (UDA)**
- **특징**: Source Domain 데이터에 라벨이 있는 상황에서 Target Domain 데이터를 라벨 없이 학습.
- **한계**: Target 데이터의 라벨 없이 분포 차이를 효과적으로 줄이기 어려움.
- - 논문: _"Maximum Classifier Discrepancy for Unsupervised Domain Adaptation"_
- 저자: Saito et al. (2018)
- 핵심: 두 분류기의 예측 불일치를 최소화하여 Target Domain에서 도메인 적응을 달성.

- **핵심 개념**: UDA는 라벨이 있는 Source Domain 데이터와 라벨이 없는 Target Domain 데이터를 이용해 Target Domain에서의 성능을 개선하는 것을 목표로 한다.
- **방법론**:
    - **Feature Alignment**: Source와 Target 도메인의 특성을 동일한 공간에서 정렬시키는 방식으로, 대표적으로 Adversarial Training(예: DANN)이 사용된다.
    - **Domain-Invariant Representations**: 두 도메인에서 공통적으로 잘 작동하는 표현을 학습한다.
    - **Reconstruction Approaches**: Target 데이터의 분포를 Source와 유사하게 변형시키거나 반대로 Source 데이터를 Target 스타일에 맞게 변형.
- **한계**: Target 도메인의 데이터 접근이 항상 보장되거나 대규모 데이터가 필요한 경우 실제 환경에 적용이 어려울 수 있음.
###### **3. Source-Free Domain Adaptation (SFDA)**
- **특징**: Source Domain 데이터 접근 없이 Target Domain 데이터만으로 적응 수행.
- **한계**: Target 데이터의 품질과 구조에 크게 의존하며 적응 과정이 불안정할 수 있음.
- - 논문: _"Source-Free Domain Adaptation via Distribution Estimation"_
- 저자: Liang et al. (2020)
- 핵심: Source 데이터 없이 Target Domain의 분포를 추정하여 모델을 적응.

- **핵심 개념**: SFDA는 Source Domain 데이터에 접근할 수 없는 상황에서 Target Domain 데이터만으로 모델을 적응시키는 방법이다.
- **방법론**:
    - **Pre-trained Model 활용**: Source Domain에서 학습된 모델을 활용하여 Target Domain의 특성에 맞게 모델의 출력 또는 중간 레이어를 조정.
    - **Self-Supervised Learning**: Target 데이터의 내재적 구조를 활용해 라벨 없이 학습.
- **장점**:
    - Source 데이터에 접근할 필요가 없어 데이터 프라이버시와 보안 문제를 해결.
    - 적은 리소스로 Target 데이터에 적응 가능.
- **한계**: Target 데이터의 라벨이 없는 상태에서 모델 수정이 제한적이며, 최적화 과정이 불안정할 수 있음.
---
###### **Domain Adaptation, UDA, SFDA의 공통 한계**

1. **라벨 의존성 부족**: Target Domain의 라벨이 없는 상황에서 정확한 피드백을 얻기 어렵다. 이는 Target Domain에서 모델 성능을 검증하거나 미세하게 조정하는 데 제한이 있다.
2. **Distribution Shift의 복잡성**: Source와 Target 사이의 분포 차이가 단순하지 않고, 구조적 변화나 새로운 클래스 등장 등의 복잡한 변화가 있는 경우 효과가 제한적이다.
3. **Generalization 한계**: 도메인 간 차이를 줄이기 위한 노력에도 불구하고, 완전히 새로운 환경에서는 여전히 성능 저하를 겪는다.
4. **데이터 품질 의존성**: Target Domain 데이터의 품질이 낮거나 노이즈가 많을 경우, 적응 과정에서 모델의 성능이 악화될 수 있다.
5. **효율성 문제**: UDA 및 SFDA는 일반적으로 대규모 데이터를 필요로 하며, 이는 계산 자원의 부담을 증가시킨다.
###### **4. Test-Time Adaptation (TTA)**
- **특징**: Test 단계에서 Target 데이터를 기반으로 실시간 적응 수행.
- **한계**: 샘플 단위 적응의 효율성과 안정성에 제약이 있을 수 있음.
- - 논문: _"Tent: Fully Test-Time Adaptation by Entropy Minimization"_
- 저자: Wang et al. (2021)
- 핵심: Batch Normalization과 Entropy Minimization을 결합하여 실시간 적응.

- **핵심 개념**: 모델이 Target 데이터에 적응하는 과정을 Test 단계에서 수행하는 방법. Source 데이터나 추가적인 사전 학습 없이 Target 데이터에서의 적응을 목표로 한다.
- **방법론**:
    - **Batch Normalization Statistics**: Test 데이터의 통계값을 통해 모델을 동적으로 조정.
    - **Entropy Minimization**: Test 데이터의 불확실성을 줄여 성능을 높이는 기법.
- **특징**:
    - 실시간 적응 가능.
    - Test 데이터에 대한 추가적인 학습 없이도 Source-Free 설정에서 작동.
- **한계**: 단일 샘플에 대해 적응하거나 테스트 시간이 길어질 수 있는 상황에서 효율성 문제가 있을 수 있음.
###### **5. Fully Test-Time Adaptation (FTTA)**
- **특징**: Test 단계에서 모든 Target 데이터를 사용해 자율적이고 지속적인 학습 수행.
- **한계**: 실시간 학습의 높은 계산 비용과 새로운 도메인에서의 불안정성.
- - 논문: _"Fully Test-Time Adaptation by Reinforcement of Self-Supervised Representations"_
- 저자: Nado et al. (2022)
- 핵심: Self-Supervised 목표를 Test 단계에서 강화하여 Target Domain의 성능을 극대화.

**Fully Test-Time Adaptation (FTTA)**는 Test-Time Adaptation(TTA)와 유사한 맥락에서 출발하지만, 보다 완전한 자율성을 갖춘 적응 방법을 목표로 한다. 이 접근법은 Test 단계에서 모델이 모든 Target 데이터에 대해 지속적으로 적응하고, 이전 데이터를 활용하지 않으며, Source 데이터에도 의존하지 않는다.

- **특징**:
    
    1. **Self-Supervised Learning 활용**: Test 단계에서 Target Domain 데이터의 특성을 활용해 라벨 없이 학습.
    2. **샘플 단위 적응**: FTTA는 각 데이터 샘플마다 독립적으로 적응을 수행하여 실시간 변화를 반영한다.
    3. **Fine-tuning 가능성**: 모델이 Test 단계에서 성능을 지속적으로 개선할 수 있다.
    4. **Source-Free**: SFDA의 연장선으로 Source Domain 데이터 없이도 효과적으로 작동.
- **장점**:
    
    - 새로운 데이터 분포에 대한 적응력을 극대화.
    - 지속적인 학습을 통해 모델이 장기간 적응 가능.
- **한계**:
    
    - 실시간 학습의 높은 계산 비용.
    - 적응 과정에서 Noise 데이터로 인해 성능 저하 가능성.
    - 완전히 새로운 도메인에서는 적응 성능이 불안정할 수 있음.
###### **6. Test-Time Training (TTT)**
- **특징**: Test 단계에서 Self-Supervised Task를 추가 학습해 Target Domain에 적응.
- **한계**: Self-Supervised Task 설계가 도메인에 따라 달라지며, 실시간 학습의 계산 비용이 높음.

- **핵심 개념**: TTT는 Test 단계에서 모델이 새로운 데이터를 볼 때마다 자체적으로 학습을 수행하는 방식으로, TTA의 확장판이다.
- **방법론**:
    - **Auxiliary Task 기반 학습**: 모델이 Test 단계에서 추가적인 학습을 통해 Target Domain에 적응.
    - **Self-Supervised Objectives**: Test 데이터의 라벨이 없는 경우에도 가능한 학습 목표(예: 데이터 복원, 특징 분해)를 설정.
- **장점**:
    - 새로운 환경에서도 모델의 성능을 실시간으로 개선 가능.
    - 지속적인 학습을 통해 도메인 변화에 대한 강건성을 제공.
- **한계**:
    - Test 단계에서 추가 연산이 요구되며, 실제 애플리케이션에서 지연(latency) 문제를 유발할 수 있음.
    - Test 데이터의 품질이 낮거나 분포가 지나치게 다를 경우 과적합 위험.


- Domain adaptation : target의 도메인이 알려져 있고, 고정되어 있다고 가정함. but, 현실 세계에서는 그렇지 않음.
- UDA(Unsupervised Domain Adaptation) : source data에 label이 있는 data와 label이 없는 target data가 모두 필요. ⇒ source데이터는 개인정보 보호때문에 사용 불가능한 경우 많음.
- SFDA(Source-Free Domain Adaptation) : 소스 데이터에 접근하지 않고, 소스 데이터에서 학습된 검출기를 타겟 도메인에 적용.
- 세 연구(domain adaptation, UDA, SFDA) 모두 target data의 도메인이 알려져 있고 고정됨.
- Test-Time Adaptation : 이미지 분류에 초점, 소스 데이터 접근을 필요로 함.
- TENT가 Fully Test-Time Adaptation을 제안 : 소스 데이터가 필요X, but 배치 단위의 테스트 샘플이 필요 + 여전히 이미지 분류에만 초점