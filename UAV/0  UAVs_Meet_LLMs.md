<h1 align="center">
  🚁 无人机（UAVs）遇上大语言模型（LLMs） 🚀
</h1>
<p align="center">
  <strong>无人机（Unmanned Aerial Vehicles）腾飞之处，即大语言模型（Large Language Models）大显身手之时！</strong>
</p>
# 🏡 关于（About）
**本文件Fork并汉化于**[Hub-Tian/UAVs_Meet_LLMs](https://github.com/Hub-Tian/UAVs_Meet_LLMs#)

本代码库配套以下研究工作：

**UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility**（无人机遇见大模型：面向智能体低空移动性的综述与展望）

如果您觉得有用，请为本项目加星 ⭐ 并 [引用](#citation) 我们的论文。

---

## 🔥 最新动态（News）
- **[2025-03-25]** 🎉 我们的论文《UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility》已被 **_Information Fusion_ 期刊接受**！敬请期待排版定稿版本（camera-ready version）。
- **[2025-01-07]** 📃 查看我们的新论文：[*UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility*](https://arxiv.org/abs/2501.02341)。
- **[2024-12-28]** 本代码库全新启动，旨在探索 **无人机 (Unmanned Aerial Vehicles, UAVs)** 与 **大语言模型 (Large Language Models, LLMs)** 之间的协同作用。我们将持续更新最新的论文、演示和见解。
- **[2024-12-27]** [Fei Lin](https://github.com/linfei-mise) 和 [Yonglin Tian](https://github.com/Hub-Tian) 整理了此列表并发布了第一个版本。

> 如果您有任何问题或建议，请随时提交 [issue](https://github.com/Hub-Tian/UAVs_Meet_LLMs/issues) 或通过 [电子邮件](yonglin.tian@ia.ac.cn) 联系我们。

---
## 无人机基础（Preliminaries for UAVs）

### 典型的无人机配置（Typical configurations of UAV）

| **类别**         | **特点**                                                     | **优点**                                                   | **缺点**                                 |
| ---------------- | ------------------------------------------------------------ | ---------------------------------------------------------- | ---------------------------------------- |
| **固定翼无人机** | 固定的机翼通过向前运动产生升力。                             | 速度快，续航时间长，飞行稳定。                             | 无法悬停，对起降区域要求高。             |
| **多旋翼无人机** | 多个旋翼提供升力和控制。                                     | 成本低，操作简单，能够垂直起降（VTOL）和悬停。             | 飞行时间有限，速度慢，有效载荷能力小。   |
| **无人直升机**   | 单旋翼或双旋翼允许垂直起飞和悬停。                           | 有效载荷能力高，抗风性好，续航时间长，可垂直起降（VTOL）。 | 结构复杂，维护成本高，比固定翼无人机慢。 |
| **混合式无人机** | 结合了固定翼和多旋翼的能力。                                 | 任务灵活，续航时间长，可垂直起降（VTOL）。                 | 机构复杂，成本较高。                     |
| **扑翼无人机**   | 使用拍击和抛掷机制进行飞行（Uses clap-and-fling mechanism）。 | 噪音低，推进效率高，机动性强。                             | 分析和控制复杂，有效载荷能力有限。       |
| **无人飞艇**     | 使用气囊提供升力的浮空器。                                   | 成本低，噪音小。                                           | 速度慢，机动性差，受风影响大。           |

### 无人机集群路径规划方法（UAV Swarm Path Planning Method）

|      **类别**      |                       **示例**                       |                         **参考文献**                         |
| :----------------: | :--------------------------------------------------: | :----------------------------------------------------------: |
|  **智能优化算法**  |           蚁群算法（Ant Colony Algorithm）           | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5498477) |
|                    |            遗传算法（Genetic Algorithm）             | [Ref](https://www.worldscientific.com/doi/abs/10.1142/S0218213017600089) |
|                    |    模拟退火算法（Simulated Annealing Algorithm）     | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8483993) |
|    **数学规划**    | 混合整数线性规划（mixed integer linear programming） | [Ref](https://journals.sagepub.com/doi/abs/10.1177/0954410015609361) |
|                    |         非线性规划（nonlinear programming）          |   [Ref](https://arc.aiaa.org/doi/abs/10.2514/6.2006-6199)    |
| **基于 AI 的方法** |              深度学习（Deep Learning）               | [Ref](https://www.sciencedirect.com/science/article/abs/pii/S1270963820311172?via%3Dihub) |
|                    |          强化学习（Reinforcement Learning）          |       [Ref](https://doi.org/10.1016/j.ast.2021.107052)       |


### 无人机集群任务分配（UAV Swarm Task Allocation）

|        **类别**        |                        **示例**                         |                         **参考文献**                         |
| :--------------------: | :-----------------------------------------------------: | :----------------------------------------------------------: |
|     **启发式算法**     | 粒子群优化算法（Particle Swarm Optimization Algorithm） |   [Ref](https://arc.aiaa.org/doi/abs/10.2514/6.2008-6837)    |
|                        |              遗传算法（Genetic Algorithm）              | [Ref](https://ieeexplore.ieee.org/abstract/document/9483937) |
|                        |      模拟退火算法（Simulated Annealing Algorithm）      | [Ref](https://iopscience.iop.org/article/10.1088/1742-6596/2246/1/012081/meta) |
|   **基于 AI 的算法**   |           强化学习（Reinforcement Learning）            |       [Ref](https://doi.org/10.1016/j.ast.2019.06.024)       |
|                        |        人工神经网络（Artificial Neural Network）        | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10670550) |
|    **数学规划方法**    |        混合整数规划（Mixed Integer Programming）        |          [Ref](https://doi.org/10.2514/6.2004-6410)          |
| **基于市场机制的方法** |        基于拍卖的算法（Auction Based Algorithm）        | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7813107) |
|                        | 基于共识的捆绑算法（Consensus Based Bundle Algorithm）  |           [Ref](https://doi.org/10.3390/s20082307)           |
|                        |          合同网络协议（Contract Net Protocol）          |           [Ref](https://doi.org/10.3390/s22124486)           |

### 无人机集群通信架构（UAV Swarm Communication Architecture）

|                           **类别**                           |                         **参考文献**                         |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
|   基于基础设施的架构（infrastructure-based architectures）   | [Ref](https://und.edu/research/rias/_files/docs/swarm_ieee.pdf) |
| 飞行自组织网络（FANET）架构（Flying Ad-hoc Network (FANET) Architectur） |      [Ref](https://doi.org/10.1016/j.adhoc.2012.12.004)      |

### 无人机集群编队控制算法（UAV Swarm Formation Control Algorithm）

|    **类别**    |                          **示例**                           |                         **参考文献**                         |
| :------------: | :---------------------------------------------------------: | :----------------------------------------------------------: |
| **集中式控制** |               虚拟结构法（Virtual Structure）               | [Ref](https://ascelibrary.org/doi/abs/10.1061/(ASCE)AS.1943-5525.0000351) |
|                |       领航者-跟随者方法（Leader-Follower Approaches）       | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=680621) |
| **分散式控制** | 分散式模型预测方法（Decentralized Model Prediction Method） | [Ref](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1429425) |
| **分布式控制** |                 行为方法（Behavior Method）                 | [Ref](https://intapi.sciendo.com/pdf/10.1515/ama-2016-0015)  |
|                |              一致性方法（Consistency Method）               |         [Ref](https://doi.org/10.3390/drones7030185)         |

## LLMs、VLMs 和 VFMs 总结（Summarization of LLMs, VLMs, and VFMs）

### LLMs (大语言模型)

| **子类别** |        **模型名称**        |                       **机构 / 作者**                        |
| :--------: | :------------------------: | :----------------------------------------------------------: |
|  **通用**  |   GPT-3, GPT-3.5, GPT-4    |                 [OpenAI](https://openai.com)                 |
|            |     Claude 2, Claude 3     |            [Anthropic](https://www.anthropic.com)            |
|            |       Mistral series       |             [Mistral AI](https://www.mistral.ai)             |
|            | PaLM series, Gemini series |          [Google Research](https://research.google)          |
|            |   LLaMA, LLaMA2, LLaMA3    |               [Meta AI](https://www.llama.com)               |
|            |           Vicuna           |           [Vicuna Team](https://vicuna.lmsys.org)            |
|            |        Qwen series         |    [Qwen Team, Alibaba Group](https://github.com/QwenLM)     |
|            |          InternLM          | [Shanghai AI Laboratory](https://github.com/InternLM/InternLM) |
|            |          BuboGPT           |    [Bytedance](https://github.com/magic-research/bubogpt)    |
|            |          ChatGLM           |          [THUKEG & THUDM](https://github.com/THUDM)          |
|            |      DeepSeek series       |          [DeepSeek](https://github.com/deepseek-ai)          |

### VLMs (视觉语言模型)

|  **子类别**  |                **模型名称**                 |                       **机构 / 作者**                        |
| :----------: | :-----------------------------------------: | :----------------------------------------------------------: |
|   **通用**   | GPT-4V, GPT-4o, GPT-4o mini, GPT o1-preview |                 [OpenAI](https://openai.com)                 |
|              |      Claude 3 Opus, Claude 3.5 Sonnet       |            [Anthropic](https://www.anthropic.com)            |
|              |                   Step-2                    |         [Jieyue Xingchen](https://www.stepfun.com/)          |
|              |        LLaVA, LLaVA-1.5, LLaVA-NeXT         |      [Liu et al.](https://github.com/haotian-liu/LLaVA)      |
|              |                  MoE-LLaVA                  |   [Lin et al.](https://github.com/PKU-YuanGroup/MoE-LLaVA)   |
|              |                  LLaVA-CoT                  |   [Xu et al.](https://github.com/PKU-YuanGroup/LLaVA-CoT)    |
|              |                  Flamingo                   | [Alayrac et al.](https://github.com/mlfoundations/open_flamingo) |
|              |                    BLIP                     |       [Li et al.](https://github.com/salesforce/BLIP)        |
|              |                   BLIP-2                    | [Li et al.](https://github.com/salesforce/LAVIS/tree/main/projects/blip2) |
|              |                InstructBLIP                 | [Dai et al.](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) |
| **视频理解** |                  LLaMA-VID                  |   [Li et al.](https://github.com/dvlab-research/LLaMA-VID)   |
|              |                   IG-VLM                    |    [Kim et al.](https://github.com/imagegridworth/IG-VLM)    |
|              |                Video-ChatGPT                | [Maaz et al.](https://github.com/mbzuai-oryx/Video-ChatGPT)  |
|              |                  VideoTree                  |    [Wang et al.](https://github.com/Ziyang412/VideoTree)     |
| **视觉推理** |                    X-VLM                    |      [Zeng et al.](https://github.com/zengyan-97/X-VLM)      |
|              |                  Chameleon                  |        [Lu et al.](https://chameleon-llm.github.io/)         |
|              |                    HYDRA                    |         [Ke et al.](https://hydra-vl4ai.github.io/)          |
|              |                   VISPROG                   | [PRIOR @ Allen Institute for AI](https://prior.allenai.org/projects/visprog) |

### VFMs (视觉基础模型)

|  **子类别**  |    **模型名称**     |                       **机构 / 作者**                        |
| :----------: | :-----------------: | :----------------------------------------------------------: |
|   **通用**   |        CLIP         |           [OpenAI](https://github.com/OpenAI/CLIP)           |
|              |        FILIP        |                          Yao et al.                          |
|              |     RegionCLIP      | [Microsoft Research](https://github.com/microsoft/RegionCLIP) |
|              |      EVA-CLIP       | [Sun et al.](https://github.com/baaivision/EVA/tree/master/EVA-CLIP) |
| **目标检测** |        GLIP         |   [Microsoft Research](https://github.com/microsoft/GLIP)    |
|              |        DINO         |    [Zhang et al.](https://github.com/IDEA-Research/DINO)     |
|              |   Grounding-DINO    | [Liu et al.](https://github.com/IDEA-Research/GroundingDINO) |
|              |       DINOv2        | [Meta AI Research, FAIR}](https://github.com/facebookresearch/dinov2) |
|              |      AM-RADIO       |          [NVIDIA](https://github.com/NVlabs/RADIO)           |
|              |       DINO-WM       |          [Zhou et al.](https://dino-wm.github.io/)           |
|              |     YOLO-World      |   [Cheng et al.](https://github.com/AILab-CVC/YOLO-World)    |
| **图像分割** |       CLIPSeg       |    [Lüdecke and Ecker](https://github.com/timojl/clipseg)    |
|              |         SAM         |    [Meta AI Research, FAIR](https://segment-anything.com)    |
|              |    Embodied-SAM     |         [Xu et al.](https://github.com/xuxw98/ESAM)          |
|              |      Point-SAM      |      [Zhou et al.](https://github.com/zyc00/Point-SAM)       |
|              | Open-Vocabulary SAM |   [Yuan et al.](https://www.mmlab-ntu.com/project/ovsam/)    |
|              |         TAP         | [Pan et al.](https://github.com/baaivision/tokenize-anything) |
|              |    EfficientSAM     |   [Xiong et al.](https://yformer.github.io/efficient-sam/)   |
|              |      MobileSAM      |  [Zhang et al.](https://github.com/ChaoningZhang/MobileSAM)  |
|              |        SAM 2        |     [Meta AI Research, FAIR](https://ai.meta.com/sam2/)      |
|              |       SAMURAI       | [University of Washington](https://github.com/yangchris11/samurai) |
|              |       SegGPT        | [Wang et al.](https://github.com/baaivision/Painter/tree/main/SegGPT) |
|              |       Osprey        |     [Yuan et al.](https://github.com/CircleRadon/Osprey)     |
|              |        SEEM         | [Zou et al.](https://github.com/UX-Decoder/Segment-Everything-Everywhere-All-At-Once) |
|              |        Seal         | [Liu et al.](https://github.com/youquanl/Segment-Any-Point-Cloud) |
|              |        LISA         |     [Lai et al.](https://github.com/dvlab-research/LISA)     |
| **深度估计** |      ZoeDepth       |      [Bhat et al.](https://github.com/isl-org/ZoeDepth)      |
|              |     ScaleDepth      |   [Zhu et al.](https://ruijiezhu94.github.io/ScaleDepth/)    |
|              |   Depth Anything    |       [Yang et al.](https://depth-anything.github.io)        |
|              |  Depth Anything V2  |     [Yang et al.](https://depth-anything-v2.github.io/)      |
|              |      Depth Pro      |        [Apple](https://github.com/apple/ml-depth-pro)        |

## 面向无人机的通用领域数据集（General-domain Datasets for UAV）

### 环境感知（Environmental Perception）

| **名称**                                                     | **年份** | **类型**                                                     | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [AirFisheye](https://collaborating.tuhh.de/ilt/airfisheye-dataset) | 2024     | 鱼眼图像、深度图像、点云、IMU（Fisheye image, Depth image, Point cloud, IMU） | 总计超过 26,000 张鱼眼图像。数据以每秒 10 帧的速度采集。     |
| [SynDrone](https://github.com/LTTM/Syndrone)                 | 2023     | 图像、深度图像、点云（Image, Depth image, Point cloud）      | 包含 72,000 个标注样本，提供 28 种像素级和对象级标注。       |
| [WildUAV](https://github.com/hrflr/wuav)                     | 2022     | 图像、视频、深度图像、元数据（Image, Video, Depth image, Metadata） | 测绘图像以 24 位 PNG 文件的形式提供，分辨率为 5280x3956。视频图像以 JPG 文件形式提供，分辨率为 3840x2160。详细说明了 16 种可能的类别标签。 |

### 事件识别（Event Recognition）

| **名称**                                       | **年份** | **类型**                  | **数量**                                                     |
| ---------------------------------------------- | -------- | ------------------------- | ------------------------------------------------------------ |
| [CapERA](https://github.com/yakoubbazi/CapEra) | 2023     | 视频、文本（Video, Text） | 2864 个视频，每个有 5 个描述，总计 14,320 条文本。每个视频持续 5 秒，以 30 帧/秒的速度捕获，分辨率为 640 × 640 像素。 |
| [ERA](https://lcmou.github.io/ERA_Dataset)     | 2020     | 视频（Video）             | 总共 2,864 个视频，包括灾难事件、交通事故、体育竞赛等 25 个类别。每个视频为 24 帧/秒，持续 5 秒。 |
| [VIRAT](https://viratdata.org/)                | 2016     | 视频（Video）             | 25 小时的静态地面视频和 4 小时的动态空中视频。涉及 23 种事件类型。 |


### 目标跟踪（Object Tracking）

| **名称**                                                     | **年份** | **类型**                                            | **数量**                                                     |
| ------------------------------------------------------------ | -------- | --------------------------------------------------- | ------------------------------------------------------------ |
| [WebUAV-3M](https://github.com/983632847/WebUAV-3M)          | 2024     | 视频、文本、音频（Video, Text, Audio）              | 4,500 个视频，总计超过 330 万帧，包含 223 个目标类别，提供自然语言和音频描述。 |
| [UAVDark135](https://vision4robotics.github.io/project/uavdark135/) | 2022     | 视频（Video）                                       | 135 个视频序列，包含超过 125,000 帧手动标注的图像。          |
| [DUT-VTUAV](https://github.com/zhang-pengyu/DUT-VTUAV)       | 2022     | RGB-T 图像（RGB-T Image）                           | 近 170 万对对齐良好的可见光-热红外 (RGB-T) 图像对，包含 500 个序列，用于揭示 RGB-T 跟踪的潜力。涵盖 13 个子类别和跨 2 个城市的 15 个场景。 |
| [TNL2K](https://github.com/wangxiao5791509/TNL2K_evaluation_toolkit) | 2022     | 视频、红外视频、文本（Video, Infrared video, Text） | 2,000 个视频序列，包含 1,244,340 帧和 663 个单词。           |
| [PRAI-1581](https://github.com/stormyoung/PRAI-1581)         | 2020     | 图像（Image）                                       | 39,461 张图像，包含 1581 个行人身份。                        |
| [VOT-ST2020/VOT-RT2020](https://votchallenge.net/vot2020/dataset.html) | 2020     | 视频（Video）                                       | 1,000 个序列，每个长度不一，平均长度约为 100 帧。            |
| [VOT-LT2020](https://votchallenge.net/vot2020/dataset.html)  | 2020     | 视频（Video）                                       | 50 个序列，每个长度约为 40,000 帧。                          |
| [VOT-RGBT2020](https://votchallenge.net/vot2020/dataset.html) | 2020     | 视频、红外视频（Video, Infrared video）             | 50 个序列，每个长度约为 40,000 帧。                          |
| [VOT-RGBD2020](https://votchallenge.net/vot2020/dataset.html) | 2020     | 视频、深度图像（Video, Depth image）                | 80 个序列，总计约 101,956 帧。                               |
| [GOT-10K](http://got-10k.aitestunion.com/)                   | 2019     | 图像、视频（Image, Video）                          | 420 个视频片段，属于 84 个目标类别和 31 个运动类别。         |
| [DTB70](https://github.com/flyers/drone-tracking)            | 2017     | 视频（Video）                                       | 70 个视频序列，每个序列由多个视频帧组成，每帧包含分辨率为 1280x720 像素的 RGB 图像。 |
| [Stanford Drone](https://cvgl.stanford.edu/projects/uav_data/) | 2016     | 视频（Video）                                       | 19,000+ 条目标轨迹，包含 6 种目标类型，约 20,000 次目标交互，40,000 次目标与环境交互，涵盖大学校园内的 100 多个场景。 |
| [COWC](https://gdo152.llnl.gov/cowc/)                        | 2016     | 图像（Image）                                       | 标注了 32,716 辆独特的车辆和 58,247 个非车辆目标。涵盖 6 个不同的地理区域。 |

### 动作识别（Action Recognition）

| **名称**                                                     | **年份** | **类型**                                                     | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Aeriform in-action](https://surbhi-31.github.io/Aeriform-in-action/) | 2023     | 视频（Video）                                                | 32 个视频，13 种动作类型，55,477 帧，40,000 个标注（callouts）。 |
| [MEVA](https://mevadata.org/)                                | 2021     | 视频、红外视频、GPS、点云（Video, Infrared video, GPS, Point cloud） | 总计 9,300 小时视频，144 小时活动注释，37 种活动类型，超过 270 万个 GPS 轨迹点。 |
| [UAV-Human](https://github.com/SUTDCV/UAV-Human)             | 2021     | 视频、夜视视频、鱼眼视频、深度视频、红外视频、骨架（Video, Night-vision video, Fisheye video, Depth video, Infrared video, Skeleton） | 67,428 个视频（155 种动作类型，119 个主体），22,476 帧标注关键点（17 个关键点），41,290 帧人员重识别（1,144 个身份），22,263 帧属性识别（如性别、帽子、背包等）。 |
| [MOD20](https://asankagp.github.io/mod20/)                   | 2020     | 视频（Video）                                                | 20 种动作类型，2,324 个视频，503,086 帧。                    |
| [NEC-DRONE](https://www.nec-labs.com/research/media-analytics/projects/unsupervised-semi-supervised-domain-adaptation-for-action-recognition-from-drones/) | 2020     | 视频（Video）                                                | 5,250 个视频，包含 256 分钟的动作视频，涉及 19 位演员和 16 个动作类别。 |
| [Drone-Action](https://asankagp.github.io/droneaction/)      | 2019     | 视频（Video）                                                | 240 个高清视频，66,919 帧，13 种动作类型。                   |
| [UAV-GESTURE](https://asankagp.github.io/uavgesture/)        | 2019     | 视频（Video）                                                | 119 个视频，37,151 帧，13 种手势类型，10 位演员。            |

### 导航与定位（Navigation and Localization）

| **名称**                                                     | **年份** | **类型**                                      | **数量**                                                     |
| ------------------------------------------------------------ | -------- | --------------------------------------------- | ------------------------------------------------------------ |
| [CityNav](https://water-cookie.github.io/city-nav-proj/)     | 2024     | 图像、文本（Image, Text）                     | 32,000 条自然语言描述和配套轨迹。                            |
| [CNER-UAV](https://github.com/zhhvvv/CNER-UAV)               | 2024     | 文本（Text）                                  | 12,000 个标注样本，包含 5 种地址标签类型（例如：建筑、单元、楼层、房间等）。 |
| [AerialVLN](https://github.com/AirVLN/AirVLN)                | 2023     | 模拟器路径、文本（Simulator path, Text）      | 25 个城市级场景，8,446 条路径，每条路径 3 条自然语言描述，总计 25,338 条指令。 |
| [DenseUAV](https://github.com/Dmmm1997/DenseUAV)             | 2023     | 图像（Image）                                 | 训练集：6,768 张无人机图像，13,536 张卫星图像。测试集：2,331 张无人机查询图像，4,662 张卫星图像。 |
| [map2seq](https://map2seq.schumann.pub/dataset/download/)    | 2022     | 图像、文本、地图路径（Image, Text, Map path） | 29,641 张全景图像，7,672 条导航指令文本。                    |
| [VIGOR](https://github.com/Jeff-Zilence/VIGOR)               | 2021     | 图像（Image）                                 | 90,618 张航空图像，238,696 张街道全景图像。                  |
| [University-1652](https://github.com/layumi/University1652-Baseline) | 2020     | 图像（Image）                                 | 1,652 栋大学建筑，72 所大学，50,218 张训练图像，37,855 张无人机查询图像，701 张卫星查询图像，以及 21,099 张普通图像和 5,580 张街景图像。 |


## 面向无人机的特定领域数据集（Domain-specific Datasets for UAV）

### 交通运输（Transportation）

| **名称**                                                     | **年份** | **类型**                                                     | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [TrafficNight](https://github.com/AIMSPolyU/TrafficNight)    | 2024     | 图像、红外图像、视频、红外视频、地图（Image, Infrared Image, Video, Infrared Video, Map） | 数据集包含 2,200 对带标注的热红外和 sRGB 图像数据，以及来自 7 个交通场景的视频数据，总时长约 240 分钟。每个场景都包含一张高精度地图，提供详细的布局和拓扑信息。 |
| [VisDrone](http://aiskyeye.com/home/)                        | 2022     | 视频、图像（Video, Image）                                   | 263 个视频，179,264 帧。10,209 张静止图像。超过 2,500,000 个目标实例标注。数据涵盖 14 个不同的城市，覆盖范围广泛的天气和光照条件。 |
| [ITCVD](https://research.utwente.nl/en/datasets/itcvd-dataset) | 2020     | 图像（Image）                                                | 总共收集了 173 张航空图像，其中训练集 135 张，包含 23,543 辆车辆，测试集 38 张，包含 5,545 辆车辆。图像之间有 60% 的区域重叠，但训练集和测试集之间没有重叠。 |
| [UAVid](https://uavid.nl/)                                   | 2020     | 图像、视频（Image, Video）                                   | 30 个视频，300 张图像，8 个语义类别标注。                    |
| [AU-AIR](https://bozcani.github.io/auairdataset)             | 2020     | 视频、GPS、高度、IMU、速度（Video, GPS, Altitude, IMU, Speed） | 32,823 帧视频，分辨率 1920x1080，30 FPS，分为 30,000 个训练验证样本和 2,823 个测试样本。8 个视频总时长约 2 小时，共有 132,034 个实例，分布在 8 个类别中。 |
| [iSAID](https://captain-whu.github.io/iSAID/)                | 2020     | 图像（Image）                                                | 总图像数：2,806 张。总实例数：655,451 个。测试集：935 张图像（不公开标注，用于服务器评估）。 |
| [CARPK](https://lafi.github.io/LPN/)                         | 2018     | 图像（Image）                                                | 1448 张图像，约 89,777 辆车辆，提供框标注。                  |
| [highD](https://levelxdata.com/highd-dataset/)               | 2018     | 视频、轨迹（Video, Trajectory）                              | 16.5 小时，110,000 辆车，5,600 次变道，45,000 公里，总计约 447 小时的车辆行驶数据；4 个预定义驾驶行为标签。 |
| [UAVDT](https://sites.google.com/view/grli-uavdt/)           | 2018     | 视频、天气、高度、摄像机角度（Video, Weather, Altitude, Camera angle） | 100 个视频，约 80,000 帧，每秒 30 帧，包含 841,500 个目标框，涵盖 2,700 个目标。 |
| [CADP](https://ankitshah009.github.io/accident_forecasting_traffic_camera) | 2016     | 视频（Video）                                                | 总时长 5.24 小时，1,416 个交通事故片段，205 个全时空标注视频。 |
| [VEDAI](https://downloads.greyc.fr/vedai)                    | 2016     | 图像（Image）                                                | 1,210 张图像（1024 × 1024 和 512 × 512 像素），9 种车辆类型，总共包含约 6,650 个目标。 |

### 遥感（Remote Sensing）

| **名称**                                                     | **年份** | **类型**                  | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------- | ------------------------------------------------------------ |
| [RET-3](https://github.com/ChenDelong1999/RemoteCLIP?utm_source=chatgpt.com) | 2024     | 图像、文本（Image, Text） | 约 13,000 个样本。包括 RSICD、RSITMD 和 UCM。                |
| [DET-10](https://github.com/ChenDelong1999/RemoteCLIP?utm_source=chatgpt.com) | 2024     | 图像（Image）             | 在目标检测数据集中，每张图像的目标数量范围为 1 到 70，总计约 80,000 个样本。 |
| [SEG-4](https://github.com/ChenDelong1999/RemoteCLIP?utm_source=chatgpt.com) | 2024     | 图像（Image）             | 分割数据集涵盖不同区域和分辨率，总计约 72,000 个样本。       |
| [DIOR](http://www.escience.cn/people/gongcheng/DIOR.html)    | 2020     | 图像（Image）             | 23,463 张图像，包含 192,472 个目标实例，涵盖 20 个类别，包括飞机、车辆、船只、桥梁等，每个类别包含约 1,200 个实例。 |
| [TGRS-HRRSD](https://github.com/CrazyStoneonRoad/TGRS-HRRSD-Dataset) | 2019     | 图像（Image）             | 总图像数：21,761 张。13 个类别，包括飞机、车辆、桥梁等。目标总数约为 53,000 个。 |
| [xView](https://xviewdataset.org/)                           | 2018     | 图像（Image）             | 有超过 100 万个目标和 60 个类别，包括车辆、建筑物、设施、船只等，分为七个父类别和几个子类别。 |
| [DOTA](https://captain-whu.github.io/DOTA/)                  | 2018     | 图像（Image）             | 2806 张图像，188,282 个目标，15 个类别。                     |
| [RSICD](https://github.com/201528014227051/RSICD_optimal)    | 2018     | 图像、文本（Image, Text） | 10,921 张图像，54,605 条描述性句子。                         |
| [HRSC2016](http://www.escience.cn/people/liuzikun/DataSet.html) | 2017     | 图像（Image）             | 3,433 个实例，总计 1,061 张图像，包括 70 张纯海洋图像和 991 张包含混合陆海区域的图像。2,876 个标记的船只目标。610 张未标记图像。 |
| [RSOD](https://github.com/RSIA-LIESMARS-WHU/RSOD-Dataset-)   | 2017     | 图像（Image）             | 包含 4 种目标类型（坦克、飞机、立交桥、操场），有 12,000 个正样本和 48,000 个负样本。 |
| [NWPU-RESISC45](http://pan.baidu.com/s/1mifR6tU)             | 2017     | 图像（Image）             | 总共 31,500 张图像，涵盖 45 个场景类别，每个类别 700 张图像，分辨率 256 × 256 像素，空间分辨率从 0.2m 到 30m。 |
| [NWPU VHR-10](https://github.com/Gaoshuaikun/NWPU-VHR-10)    | 2014     | 图像（Image）             | 800 张高分辨率图像，其中 650 张包含目标，150 张是背景图像，涵盖 10 个类别（如飞机、船只、桥梁等），总计超过 3,000 个目标。 |


### 农业（Agriculture）

| **名称**                                                     | **年份** | **类型**                             | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------------------ | ------------------------------------------------------------ |
| [WEED-2C](https://github.com/EvertonTetila/WEED2C-Dataset/?tab=readme-ov-file) | 2024     | 图像（Image）                        | 包含 4,129 个标注样本，涵盖 2 种杂草。                       |
| [CoFly-WeedDB](https://github.com/CoFly-Project/CoFly-WeedDB/blob/main/README.md?utm_source=chatgpt.com) | 2023     | 图像、健康数据（Image, Health data） | 包含 201 张航空图像、3 种受干扰行作物（棉花）的不同杂草类型及其对应的标注图像。 |
| [Avo-AirDB](https://github.com/LCSkhalid/Avo-AirDB)          | 2022     | 图像（Image）                        | 984 张高分辨率 RGB 图像（5472 × 3648 像素），其中 93 张具有详细的多边形标注，分为 3 到 4 个类别（小、中、大和背景）。 |

### 工业（Industry）

| **名称**                                                     | **年份** | **类型**      | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------- | ------------------------------------------------------------ |
| [UAPD](https://github.com/tantantetetao/UAPD-Pavement-Distress-Dataset) | 2021     | 图像（Image） | 原始数据中有 2,401 张裂缝图像，数据增强后有 4,479 张裂缝图像。 |
| [InsPLAD](https://github.com/andreluizbvs/InsPLAD/)          | 2023     | 图像（Image） | 10,607 张无人机图像，包含 17 类电力资产，总共有 28,933 个标注实例，以及 5 种资产的缺陷标签，总共 402 个缺陷样本，分为 6 种缺陷类型。 |

### 应急响应（Emergency Response）

| **名称**                                                     | **年份** | **类型**                  | **数量**                                                     |
| ------------------------------------------------------------ | -------- | ------------------------- | ------------------------------------------------------------ |
| [AFID](https://purr.purdue.edu/publications/4105/1)          | 2023     | 图像（Image）             | 总共 816 张图像，分辨率为 2720 × 1536 和 2560 × 1440。包含 8 个语义分割类别。 |
| [FloodNet](https://github.com/BinaLab/FloodNet-Supervised_v1.0) | 2021     | 图像、文本（Image, Text） | 整个数据集有 2,343 张图像，分为训练集（约 60%）、验证集（约 20%）和测试集（约 20\%）。语义分割标签包括：背景、淹没的建筑物、未淹没的建筑物、淹没的道路、未淹没的道路、水、树木、车辆、水池、草地。 |
| [Aerial SAR](https://www.leadingindia.ai/data-set)           | 2020     | 图像（Image）             | 2,000 张图像，包含 30,000 个动作实例，涵盖多种人类行为。     |

### 军事（Military）

| **名称**                                 | **年份** | **类型**                  | **数量**                                      |
| ---------------------------------------- | -------- | ------------------------- | --------------------------------------------- |
| [MOCO](https://github.com/Panlizhi/MOCO) | 2024     | 图像、文本（Image, Text） | 7,449 张图像，37,245 条文字描述（captions）。 |

### 野生动物（Wildlife）

| **名称**                                   | **年份** | **类型**      | **数量**                                               |
| ------------------------------------------ | -------- | ------------- | ------------------------------------------------------ |
| [WAID](https://github.com/xiaohuicui/WAID) | 2023     | 图像（Image） | 14,375 张无人机图像，涵盖 6 种野生动物和多种环境类型。 |

### 无人机检测（Drone Detection）

| **名称**                                                     | **年份** | **类型**                                     | **数量**                                                     |
| ------------------------------------------------------------ | -------- | -------------------------------------------- | ------------------------------------------------------------ |
| [DroneRFa](https://data.mendeley.com/datasets/f4c2b4n755/1)  | 2024     | 射频信号（RF signal）                        | 包括 24 种无人机信号（9 种室外采集和 15 种室内采集）和 1 种背景信号，涵盖 3 个 ISM 频段。 |
| [IDTDSAT](https://www.scidb.cn/en/detail?dataSetId=720626420933459968) | 2019     | 红外图像、轨迹（Infrared image, Trajectory） | 22 段红外图像序列，总帧数 16,177 帧，总目标数 16,944 个，30 条轨迹；图像分辨率 256 × 256 像素。 |
| [DTDAOTRES](https://www.scidb.cn/en/detail?dataSetId=720626420979597312) | 2019     | 雷达（Radar）                                | 15 个片段，8.76 GB。                                         |

## 无人机开放平台（Open Platforms for UAVs）

| **名称**                                                   | **出版物**                                                   |
| ---------------------------------------------------------- | ------------------------------------------------------------ |
| [AirSim](https://microsoft.github.io/AirSim/)              | Airsim: 高保真视觉和物理模拟，用于自动驾驶车辆（High-fidelity visual and physical simulation for autonomous vehicles） |
| [Carla](https://carla.org/)                                | CARLA: 一个开放的城市驾驶模拟器（An open urban driving simulator） |
| [NVIDIA Isaac Sim](https://developer.nvidia.com/isaac/sim) |                                                              |
| [AerialVLN Simulator](https://github.com/AirVLN/AirVLN)    | Aerialvln: 无人机视觉与语言导航（Vision-and-language navigation for uavs） |
| [Embodied City](https://embodied-city.fiblab.net/)         | EmbodiedCity: 用于现实世界城市环境中具身智能体的基准平台（A Benchmark Platform for Embodied Agent in Real-world City Environment） |

## 基于 FM 的无人机系统在各种任务中的进展（Advances of FM-based UAV Systems in Various Tasks）

### 视觉感知（Visual Perception）

| 标题                                                         | 类型        | 出版物                                                       | 代码                                                         |
| ------------------------------------------------------------ | ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Li et al. (A Benchmark for UAV-View Natural Language-Guided Tracking)（无人机视角自然语言引导跟踪基准） | VFM         | [ _MDPI_ ](https://www.mdpi.com/2079-9292/13/9/1706)         | [ _GitHub_ ](https://github.com/Lich-King000/UAVNLT)         |
| Ma et al. (Applying Unsupervised Semantic Segmentation to High-Resolution UAV Imagery for Enhanced Road Scene Parsing)（将无监督语义分割应用于高分辨率无人机图像以增强道路场景解析） | VFM         | [ _Arxiv_ ](https://arxiv.org/abs/2402.02985)                | -                                                            |
| Limberg et al. (Leveraging YOLO-World and GPT-4V LMMs for Zero-Shot Person Detection and Action Recognition in Drone Imagery)（利用 YOLO-World 和 GPT-4V LMM 进行无人机图像中的零样本人物检测和动作识别） | VFM+VLM     | [ _Arxiv_ ](https://arxiv.org/abs/2404.01571)                | -                                                            |
| Kim et al. (Weather-Aware Drone-View Object Detection Via Environmental Context Understanding)（通过环境上下文理解实现天气感知无人机视角目标检测） | VLM+VFM     | [ _ICIP 2024_ ](https://ieeexplore.ieee.org/abstract/document/10647388?casa_token=5WOlhDhGgSMAAAAA:nwp96nnFaZE9U3t5XnZmLPYr9f3Lw1YUKx6w4qyKx5F6Gzwa9uwmMUsKc2IX6gdvomLZ7Dcf9l9u) | -                                                            |
| LGNet (Shooting condition insensitive unmanned aerial vehicle object detection)（对拍摄条件不敏感的无人机目标检测） | VFM         | [ _Expert Systems with Applications_ ](https://www.sciencedirect.com/science/article/pii/S0957417424000861?casa_token=3A-yp3URHJ4AAAAA:MHJXhYWUpX_mZMUggAo5oSa9FxpJsYdqbo940lZj-gfb5XuPOHAEdMQ1ZiyTEXir1kQUfjQMRA) | -                                                            |
| Sakaino et al. (Dynamic Texts From UAV Perspective Natural Images)（来自无人机视角的自然图像中的动态文本） | VLM+VFM     | [ _ICCV 2023_ ](https://openaccess.thecvf.com/content/ICCV2023W/OpenSUN3D/html/Sakaino_Dynamic_Texts_From_UAV_Perspective_Natural_Images_ICCVW_2023_paper.html) | -                                                            |
| COMRP (Unsupervised semantic segmentation of high-resolution UAV imagery for road scene parsing)（高分辨率无人机图像的无监督语义分割以进行道路场景解析） | VFM         | [ _Arxiv_ ](https://arxiv.org/abs/2402.02985)                | [ _GitHub_ ](https://github.com/CHDyshli/unsupervised-road-parsing) |
| CrossEarth (CrossEarth: Geospatial Vision Foundation Model for Domain Generalizable Remote Sensing Semantic Segmentation)（CrossEarth：用于域泛化遥感语义分割的地理空间视觉基础模型） | VFM         | [ _Arxiv_ ](https://arxiv.org/abs/2410.22629)                | [ _GitHub_ ](https://github.com/Cuzyoung/CrossEarth)         |
| TanDepth (TanDepth: Leveraging Global DEMs for Metric Monocular Depth Estimation in UAVs)（TanDepth：利用全球数字高程模型（DEM）进行无人机中的度量单目深度估计） | VFM         | [ _Arxiv_ ](https://arxiv.org/abs/2409.05142)                | [ _GitHub_ ](https://github.com/hrflr/uavid-3d-scenes)       |
| DroneGPT (DroneGPT: Zero-shot Video Question Answering For Drones)（DroneGPT：无人机零样本视频问答） | VLM+LLM+VFM | [ _CVDL 2024_ ](https://dl.acm.org/doi/abs/10.1145/3653804.3654608?casa_token=CtmHh5WiSTQAAAAA:3D70U8Z_CHJ1jrx9u4zduBfCi91JI3lFGVA3ZhCDQVOgEcSEaYuzGxKLWHX7fE6a3YviSkjat4mPug) | -                                                            |
| de Zarzà et al. (Socratic video understanding on unmanned aerial vehicles)（无人机上的苏格拉底式视频理解） | LLM         | [ _Procedia Computer Science_ ](https://www.sciencedirect.com/science/article/pii/S1877050923011560) | -                                                            |
| AeroAgent (Agent as Cerebrum, Controller as Cerebellum: Implementing an Embodied LMM-based Agent on Drones)（Agent 作大脑，控制器作小脑：在无人机上实现基于具身 LMM 的智能体） | VLM         | [ _Arxiv_ ](https://arxiv.org/abs/2311.15033)                | -                                                            |
| RS-LLaVA (Rs-llava: A large vision-language model for joint captioning and question answering in remote sensing imagery)（RS-LLaVA：用于遥感图像联合字幕生成和问答的大型视觉语言模型） | VLM         | [ _MDPI_ ](https://www.mdpi.com/2072-4292/16/9/1477)         | -                                                            |
| GeoRSCLIP (RS5M and GeoRSCLIP: A large scale vision-language dataset and a large vision-language model for remote sensing)（RS5M 和 GeoRSCLIP：用于遥感的超大规模视觉语言数据集和大型视觉语言模型） | VFM         | [ _IEEE Transactions on Geoscience and Remote Sensing_ ](https://ieeexplore.ieee.org/abstract/document/10679571?casa_token=TyNG8Ytg_mIAAAAA:byAkV0_chtOVtdNjFaTmNA3EZIMH-cLQ38SP-CmAFrKcoPRyuNCx9DGqq54f1kOb32g7I3P5rHxRDw) | [ _GitHub_ ](https://github.com/om-ai-lab/RS5M)              |
| SkyEyeGPT (Skyeyegpt: Unifying remote sensing vision-language tasks via instruction tuning with large language model)（SkyEyeGPT：通过大型语言模型指令微调统一遥感视觉语言任务） | VFM+LLM     | [ _Arxiv_ ](https://arxiv.org/abs/2401.09712)                | [ _GitHub_ ](https://github.com/ZhanYang-nwpu/SkyEyeGPT)     |
| AirVista (AirVista: Empowering UAVs with 3D Spatial Reasoning Abilities Through a Multimodal Large Language Model Agent)（AirVista：通过多模态大语言模型智能体赋予无人机 3D 空间推理能力） | VFM+VLM     | [ _ITSC2024_ ](https://doi.org/10.1109/ITSC58415.2024.10919532) | -                                                            |
### 视觉与语言导航（VLN）

| 标题                                                         |        类型 | 出版物                                                       | 代码                                                      |
| ------------------------------------------------------------ | ----------: | ------------------------------------------------------------ | --------------------------------------------------------- |
| Neuro-LIFT (Neuro-LIFT: A Neuromorphic, LLM-based Interactive Framework for Autonomous Drone FlighT at the Edge)（Neuro-LIFT：一个基于神经形态和大模型的交互式框架，用于边缘自主无人机飞行） |         LLM | [ _Arxiv_ ](https://arxiv.org/abs/2501.19259v1)              | -                                                         |
| NaVid (Navid: Video-based vlm plans the next step for vision-and-language navigation)（NaVid：基于视频的视觉语言模型为视觉与语言导航规划下一步） |     VFM+LLM | [ _Arxiv_ ](https://arxiv.org/abs/2402.15852)                | -                                                         |
| VLN-MP (Why Only Text: Empowering Vision-and-Language Navigation with Multi-modal Prompts)（为何只有文本：使用多模态提示增强视觉与语言导航） |         VFM | [ _Arxiv_ ](https://arxiv.org/abs/2406.02208)                | [ _GitHub_ ](https://github.com/honghd16/VLN-MP)          |
| Gao et al. (Aerial Vision-and-Language Navigation via Semantic-Topo-Metric Representation Guided LLM Reasoning)（通过语义-拓扑-度量表示引导的大模型推理实现空中视觉与语言导航） |     VFM+LLM | [ _Arxiv_ ](https://arxiv.org/abs/2410.08500)                | -                                                         |
| MGP (CityNav: Language-Goal Aerial Navigation Dataset with Geographic Information)（CityNav：具有地理信息的语言目标空中导航数据集） |     LLM+VFM | [ _Arxiv_ ](https://arxiv.org/abs/2406.14240)                | [ _GitHub_ ](https://github.com/water-cookie/citynav)     |
| UAV Navigation LLM (Towards Realistic UAV Vision-Language Navigation: Platform, Benchmark, and Methodology)（迈向真实的无人机视觉语言导航：平台、基准和方法） |     LLM+VFM | [ _Arxiv_ ](https://arxiv.org/abs/2410.07087)                | [ _GitHub_ ](https://prince687028.github.io/OpenUAV/)     |
| GOMAA-Geo (GOMAA-Geo: GOal Modality Agnostic Active Geo-localization)（GOMAA-Geo：目标模态无关主动地理定位） |     LLM+VFM | [ _Arxiv_ ](https://arxiv.org/abs/2406.01917)                | [ _GitHub_ ](https://github.com/mvrl/GOMAA-Geo/tree/main) |
| NavAgent (NavAgent: Multi-scale Urban Street View Fusion For UAV Embodied Vision-and-Language Navigation)（NavAgent：用于无人机具身视觉与语言导航的多尺度城市街景融合） | LLM+VFM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2411.08579)                | -                                                         |
| ASMA (ASMA: An Adaptive Safety Margin Algorithm for Vision-Language Drone Navigation via Scene-Aware Control Barrier Functions)（ASMA：通过场景感知控制障碍函数实现视觉语言无人机导航的自适应安全裕度算法） |     LLM+VFM | [ _Arxiv_ ](https://arxiv.org/abs/2409.10283)                | -                                                         |
| Zhang et al. (Demo Abstract: Embodied Aerial Agent for City-level Visual Language Navigation Using Large Language Model)（演示摘要：使用大型语言模型进行城市级视觉语言导航的具身空中智能体） |     VFM+LLM | [ _IPSN 2024_ ](https://ieeexplore.ieee.org/abstract/document/10577302?casa_token=n2FU0mxrCvoAAAAA:E86JlA4m98x2f09d0VZ5199dx8gH-kxUfVA2LU7rjWd5s4alCDoQdHH67Vc5gbhnSI_W1tQNjdpHLA) | -                                                         |
| Chen et al. (Vision-Language Navigation for Quadcopters with Conditional Transformer and Prompt-based Text Rephraser)（带条件 Transformer 和基于提示文本复述器的四旋翼无人机视觉语言导航） |         LLM | [ _MMAsia 2023_ ](https://dl.acm.org/doi/abs/10.1145/3595916.3626450?casa_token=fGnueKEkiZsAAAAA:roEaZ3SHZ8UW9-i2vy_5pv_mwLlDVv4cL-MHxuGNQCKlOg9PuaX_vsUZ6WiRz4lOnJbCq-DxKycZGg) | -                                                         |
| CloudTrack (CloudTrack: Scalable UAV Tracking with Cloud Semantics)（CloudTrack：基于云语义的可扩展无人机跟踪） |     VFM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2409.16111)                | -                                                         |
| NEUSIS (NEUSIS: A Compositional Neuro-Symbolic Framework for Autonomous Perception, Reasoning, and Planning in Complex UAV Search Missions)（NEUSIS：用于复杂无人机搜索任务中自主感知、推理和规划的组合神经-符号框架） |     VFM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2409.10196)                | -                                                         |
| Say-REAPEx (Say-REAPEx: An LLM-Modulo UAV Online Planning Framework for Search and Rescue)（Say-REAPEx：用于搜救的 LLM-Modulo 无人机在线规划框架） |         LLM | [ _Openreview_ ](https://openreview.net/forum?id=9WdUqvE03f) | -                                                         |
| OpenFLY (OpenFly: A Versatile Toolchain and Large-scale Benchmark for Aerial Vision-Language Navigation)（OpenFLY：用于空中视觉语言导航的多功能工具链和大规模基准） |     LLM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2502.18041v3)              | [ _GitHub_ ](https://shailab-ipec.github.io/openfly/)     |

### 规划（Planning）

| 标题                                                         |        类型 | 出版物                                                       | 代码                                              |
| ------------------------------------------------------------ | ----------: | ------------------------------------------------------------ | ------------------------------------------------- |
| TypeFly (Typefly: Flying drones with large language model)（Typefly：使用大型语言模型控制无人机飞行） |         LLM | [ _Arxiv_ ](https://arxiv.org/abs/2312.14950)                | -                                                 |
| SPINE (SPINE: Online Semantic Planning for Missions with Incomplete Natural Language Specifications in Unstructured Environments)（SPINE：在非结构化环境中针对不完整自然语言规范任务的在线语义规划） | LLM+VFM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2410.03035)                | -                                                 |
| LEVIOSA (LEVIOSA: Natural Language-Based Uncrewed Aerial Vehicle Trajectory Generation)（LEVIOSA：基于自然语言的无人机轨迹生成） |         LLM | [ _MDPI_ ](https://www.mdpi.com/2079-9292/13/22/4508)        | [ _GitHub_ ](https://github.com/sesem738/Leviosa) |
| TPML (TPML: Task Planning for Multi-UAV System with Large Language Models)（TPML：使用大型语言模型进行多无人机系统任务规划） |         LLM | [ _ICCA 2023_ ](https://ieeexplore.ieee.org/abstract/document/10591846?casa_token=xa1KFvlHFzUAAAAA:LBGOwvV_4iUcNLewToZCjFnr5aIUnReWyTvKyZsuY_nnGsk_eh8u1TW6MHpQ1NEF5pO-VPzAVovAuHA) | -                                                 |
| REAL (Real: Resilience and adaptation using large language models on autonomous aerial robots)（REAL：在自主飞行机器人上使用大型语言模型实现弹性和适应性） |         LLM | [ _Arxiv_ ](https://arxiv.org/abs/2311.01403)                | -                                                 |
| Liu et al. (Multi-Agent Formation Control Using Large Language Models)（使用大型语言模型进行多智能体编队控制） |         LLM | [ _Techrxiv_ ](https://www.techrxiv.org/doi/full/10.36227/techrxiv.172954477.70259514) | -                                                 |
| AutoHMA-LLM (AutoHMA-LLM: Efficient Task Coordination and Execution in Heterogeneous Multi-Agent Systems Using Hybrid Large Language Models)（AutoHMA-LLM：使用混合大型语言模型实现异构多智能体系统中高效任务协调和执行） |         LLM | [ _IEEE_ ](https://ieeexplore.ieee.org/abstract/document/10839354) | -                                                 |
| ACMA (Agent in the Sky: Intelligent Multi-Agent Framework for Autonomous HAPS Coordination and Real-World Event Adaptation)（天空中的智能体：用于自主高空平台（HAPS）协调和现实世界事件适应的智能多智能体框架） |         LLM | [ _AAAI_ ](https://openreview.net/forum?id=MHbz86z3h5)       | -                                                 |
| UAV-VLA (UAV-VLA: Vision-Language-Action System for Large Scale Aerial Mission Generation)（UAV-VLA：用于大规模空中任务生成的视觉-语言-动作系统） |     LLM+VLM | [ _Arxiv_ ](https://arxiv.org/abs/2501.05014)                | -                                                 |

### 飞行控制（Flight Control）

| 标题                                                         | 类型 | 出版物                                                       | 代码                                                         |
| ------------------------------------------------------------ | ---: | ------------------------------------------------------------ | ------------------------------------------------------------ |
| PromptCraft (Chatgpt for robotics: Design principles and model abilities)（用于机器人的 ChatGPT：设计原则和模型能力） |  LLM | [ _IEEE Access_ ](https://ieeexplore.ieee.org/abstract/document/10500490) | [ _GitHub_ ](https://github.com/microsoft/PromptCraft-Robotics) |
| Zhong et al. (A safer vision-based autonomous planning system for quadrotor uavs with dynamic obstacle trajectory prediction and its application with llms)（一种更安全的基于视觉的四旋翼无人机自主规划系统，具有动态障碍物轨迹预测及其在 LLM 中的应用） |  LLM | [ _WACV 2024_ ](https://openaccess.thecvf.com/content/WACV2024W/LLVM-AD/html/Zhong_A_Safer_Vision-Based_Autonomous_Planning_System_for_Quadrotor_UAVs_With_WACVW_2024_paper.html) | -                                                            |
| Tazir et al. (From words to flight: Integrating openai chatgpt with px4/gazebo for natural language-based drone control)（从文字到飞行：整合 OpenAI ChatGPT 与 PX4/Gazebo 进行基于自然语言的无人机控制） |  LLM | [ _WCSE 2023_ ](https://www.researchgate.net/profile/Mohamed-Lamine-Tazir/publication/372028642_From_Words_to_Flight_Integrating_OpenAI_ChatGPT_with_PX4Gazebo_for_Natural_Language-Based_Drone_Control/links/64a2ef5295bbbe0c6e0dda04/From-Words-to-Flight-Integrating-OpenAI-ChatGPT-with-PX4-Gazebo-for-Natural-Language-Based-Drone-Control.pdf) | -                                                            |
| Phadke et al. (Integrating Large Language Models for UAV Control in Simulated Environments: A Modular Interaction Approach)（在模拟环境中集成大型语言模型进行无人机控制：一种模块化交互方法） |  LLM | [ _Arxiv_ ](https://arxiv.org/abs/2410.17602)                | -                                                            |
| EAI-SIM (EAI-SIM: An Open-Source Embodied AI Simulation Framework with Large Language Models)（EAI-SIM：一个带有大型语言模型的开源具身 AI 模拟框架） |  LLM | [ _ICCA 2024_ ](https://ieeexplore.ieee.org/abstract/document/10591865?casa_token=Q8xpKHwtDaAAAAAA:d8MNPpg5Q86ZlC9NkMcbPOZ58K_ZewmAHOOjC8KTgHL6VODSyYUdhoQUcOHyUOLl6NH79L_fkcBxa6Y) | [ _GitHub_ ](https://github.com/PengICS/eai_sim)             |
| TAIiST (TAIiST CPS-UAV at the SBFT Tool Competition 2024)（TAIiST CPS-UAV 参加 SBFT 2024 工具竞赛） |  LLM | [ _SBFT 2024_ ](https://dl.acm.org/doi/abs/10.1145/3643659.3643936) | [ _GitHub_ ](https://github.com/Trusted-AI-in-System-Test)   |
| Swarm-GPT (Swarm-gpt: Combining large language models with safe motion planning for robot choreography design)（Swarm-GPT：结合大型语言模型和安全运动规划进行机器人编舞设计） |  LLM | [ _Arxiv_ ](https://www.dynsyslab.org/wp-content/papercite-data/pdf/jiao-neurips23.pdf) | -                                                            |
| FlockGPT (FlockGPT: Guiding UAV Flocking with Linguistic Orchestration)（FlockGPT：通过语言编排引导无人机集群飞行） |  LLM | [ _Arxiv_ ](https://arxiv.org/abs/2405.05872)                | -                                                            |
| CLIPSwarm (CLIPSwarm: Generating Drone Shows from Text Prompts with Vision-Language Models)（CLIPSwarm：使用视觉语言模型从文本提示生成无人机表演） |  VFM | [ _Arxiv_ ](https://arxiv.org/abs/2403.13467)                | -                                                            |

### 基础设施（Infrastructures）

| 标题                                                         |    类型 | 出版物                                                       | 代码                                                         |
| ------------------------------------------------------------ | ------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
| DTLLM-VLT (DTLLM-VLT: Diverse Text Generation for Visual Language Tracking Based on LLM)（DTLLM-VLT：基于 LLM 的视觉语言跟踪多样化文本生成） | VFM+LLM | [ _CVPR 2024_ ](https://openaccess.thecvf.com/content/CVPR2024W/VDU/html/Li_DTLLM-VLT_Diverse_Text_Generation_for_Visual_Language_Tracking_Based_on_CVPRW_2024_paper.html) | -                                                            |
| Yao et al. (Can llm substitute human labeling? a case study of fine-grained chinese address entity recognition dataset for uav delivery)（LLM 能否取代人工标注？以无人机配送细粒度中文地址实体识别数据集为例） |     LLM | [ _Companion Proceedings of the ACM Web Conference 2024_ ](https://dl.acm.org/doi/abs/10.1145/3589335.3651446?casa_token=mJzJVbxcOSUAAAAA:TUrPUIvFd7m7-LyBbn0UZ2-8ZuOgdUUGTHO3-TvQj1zrdd_HqIcz_Zbud7NuS8n6aVSKNM6pr3d3ue0) | [ _GitHub_ ](https://github.com/zhhvvv/CNER-UAV)             |
| GPG2A (Cross-View Meets Diffusion: Aerial Image Synthesis with Geometry and Text Guidance)（跨视角与扩散模型相遇：基于几何和文本引导的航空图像合成） |     LLM | [ _Arxiv_ ](https://arxiv.org/abs/2408.04224)                | [ _GitLap_ ](https://gitlab.com/vail-uvm/GPG2A)              |
| AeroVerse (AeroVerse: UAV-Agent Benchmark Suite for Simulating, Pre-training, Finetuning, and Evaluating Aerospace Embodied World Models)（AeroVerse：用于模拟、预训练、微调和评估航空航天具身世界模型的无人机-智能体基准套件） | VLM+LLM | [ _Arxiv_ ](https://arxiv.org/abs/2408.15511)                | -                                                            |
| Tang et al. (Defining and Evaluating Physical Safety for Large Language Models)（定义和评估大型语言模型的物理安全） |     LLM | [ _Arxiv_ ](https://arxiv.org/abs/2411.02317)                | [ _Hugging face_ ](https://huggingface.co/datasets/TrustSafeAI/llm_physical_safety_benchmark) |
| Xu et al. (Emergency Networking Using UAVs: A Reinforcement Learning Approach with Large Language Model)（使用无人机进行应急组网：基于大型语言模型的强化学习方法） |     LLM | [ _IPSN 2024_ ](https://ieeexplore.ieee.org/abstract/document/10577381?casa_token=Mmd9-ZDptTUAAAAA:q6shHGKcyH-748YODzx40WlYoLaswZcNK9Ik0z741pTnZX1inG9G0nQm5eBuaMnUl7T9eGgBdszs) | -                                                            |
| LLM-RS (Real-time Integration of Fine-tuned Large Language Model for Improved Decision-Making in Reinforcement Learning)（实时集成微调大型语言模型以改进强化学习中的决策） |     LLM | [ _IJCNN 2024_ ](https://ieeexplore.ieee.org/abstract/document/10650538?casa_token=nT06OMN91ZEAAAAA:rqTAbczP0wz615qxgPtIitMnscaFSUoA_Vs5hJ58uiVGXu4gNEqntpK9AfYfVXq89-JsZsIO_Vfh) | -                                                            |
| Pineli et al. (Evaluating Voice Command Pipelines for Drone Control: From STT and LLM to Direct Classification and Siamese Networks)（评估用于无人机控制的语音命令管线：从语音转文本（STT）和 LLM 到直接分类和 Siamese 网络） |     LLM | [ _Arxiv_ ](https://arxiv.org/abs/2407.08658)                | -                                                            |

## 贡献者（Contributors）
我们感谢以下贡献者创建、维护和整理本代码库中的表格：

- **Yonglin Tian**
- **Fei Lin**
- **Yiduo Li**
- **Tengchao Zhang**
- **Xuan Fu**

如果您对本代码库有任何疑问，请随时联系 **Yonglin Tian** [📧](mailto:yonglin.tian@ia.ac.cn) 或 **Fei Lin** [📧](mailto:feilin@ieee.org)。

*(如果您想为本代码库做出贡献，请提出 Issue 或 Pull Request。)*

---

## 引用（Citation）
如果您认为本代码库有用，请考虑引用以下论文：

```bibtex
@misc{tian2025uavsmeetllmsoverviews,
      title={UAVs Meet LLMs: Overviews and Perspectives Toward Agentic Low-Altitude Mobility}, 
      author={Yonglin Tian and Fei Lin and Yiduo Li and Tengchao Zhang and Qiyao Zhang and Xuan Fu and Jun Huang and Xingyuan Dai and Yutong Wang and Chunwei Tian and Bai Li and Yisheng Lv and Levente Kovács and Fei-Yue Wang},
      year={2025},
      eprint={2501.02341},
      archivePrefix={arXiv},
      primaryClass={cs.RO},
      url={[https://arxiv.org/abs/2501.02341](https://arxiv.org/abs/2501.02341)}, 
}