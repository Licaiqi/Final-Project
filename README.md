# Final-Project
How to apply LLMs in specific domains.

医疗
=====

应用方向
-----
_____

近年来, 人工智能大模型快速发展, 它们的参数量和所用于预训练的数据量已达到几百上千亿级别。经预训练后, 这些大模型在各种下游任务中展现出强大的泛化能力。在医疗领域中存在大量模态种类丰富的数据，且呈现出多学科、跨领域的特点，而大模型的长项就是对多类数据进行整合总结、分析判断和自动摘要。在前沿研究推动下，大模型扎根医疗，已经有了明朗的趋势。在行业发展方面，大模型正在被引入临床诊断决策、病例数据管理等领域，衍生出一系列AI应用。同时大模型也可能在生物信息学，医疗诊断，医学成像和视觉，医疗信息学，医学教育，公共卫生和医疗机器人等方面发挥重要作用。

应用难点
-----
_____
从目前来看，虽然大型人工智能模型呈现出了非常可观的应用前景，它们的发展和在生物医学，临床，医疗等领域的运用还存在着诸多挑战和潜在风险。
例如安全性方面，由于行业特殊性，医疗机构对于数据和隐私安全极其重视，任何医疗数据都要在安全可控的内网环境存储和传输，因此医疗大模型更适合私有化的部署环境。而大模型的训练和推理，要堆叠大量的专用加速芯片，成本高昂。要想让医疗大模型部署落地，如何降低大模型的算力成本就是必须要考虑的问题。模型剪枝与量化是两种较为常用的降低算力成本的方法。对于大型深度学习模型，可以通过模型剪枝（pruning）来减少参数数量，从而减小模型的计算和存储开销。或者通过量化（quantization）来减少参数的精度，将训练好的模型的权值、激活值等从高精度数据格式 (如 FP32 等) 转化为低精度数据格式 (如 INT4 /INT8 等)，从而降低推理过程中对内存等资源的需求，让平台可以容纳更大参数规模的大模型，并大幅提升推理速度。在某些应用场景中用一些可以接受的精度损失，换取模型的算力成本降低。除此之外，在数据、算法、可信度、隐私性、公平性、透明度、可解释性、可持续性、规范等方面大模型也面临不少挑战。


大模型应用实例
-----
_____
*谷歌医疗大模型（Med-PaLM）*  
根据谷歌和DeepMind的科研人员的研究结果，一组临床医生对谷歌和DeepMind团队的医疗大模型Med-PaLM回答的评分高达92.6%，与现实中人类临床医生的水平（92.9%）相当。

*BioMedLM（PubMedGPT）*  
经训练可以解释生物医学语言，在美国医疗执照考试 (USMLE)的医疗问答文本上取得了最先进的结果。

*ChatDoctor*  
使用医学领域知识在大型语言模型LLaMA上进行微调的医疗大模型，在精度、召回率和F1方面超过ChatGPT。

*DoctorGLM*  
基于 ChatGLM-6B的中文问诊模型，实现了包括lora、p-tuningv2等微调及部署。

*XrayGLM*
首个会看胸部X光片的中文多模态医学大模型，在医学影像诊断和多轮交互对话上显示出了非凡的潜力。

**从目前来看，大模型的发展，第一应该为发展性能，比如，扩大模型和数据集的规模，进行多模态、多任务的预训练；第二，则是挖掘已有大型人工智能模型的潜力，比如通过prompt engineering, fine-tuning, linear probing等， 来进一步探索它们尚未被人们知悉的能力。**

法律
=====

应用方向
-----
______
法律大模型是指专门针对法律领域的人工智能模型，它在通用大模型的基础上，使用高质量的法律数据进行微调，以提高模型在法律问答、文本生成、案例分析等任务上的专业性和准确性。法律大模型的应用场景主要有：法律咨询服务（通过对话的方式，为用户提供针对具体法律问题的咨询和建议，并给出相关的法律依据和解释），法律文书生成（帮助用户起草多种法律文书，并提供必要的修改和优化建议），法律知识发现（帮助用户发现和挖掘有价值的法律知识，如法律条款、判例、案例分析等，并进行归纳和总结），法律智能监督（帮助用户进行法律智能监督，根据用户的需求，实现线索的办理管控、线索共享与应用、线索应用成效分析等功能）。

法律大模型应该具备的特点以及面对的挑战
-----
______
法律领域的大模型本质是复杂决策，而非仅仅是开放式对话模型，需要具备丰富的专业知识，能够推断各类复杂案件场景，具备综合任务的拆解能力和宏观态势的研判能力。目前法律大模型在很多方面都面对挑战，例如高质量数据的收集；技术的迭代速度快导致的对研究和跟进的高要求；很难建立一个完善的开发体系等等。现阶段，设计合理的模型架构、将大模型与知识图谱技术结合，应用在学习阶段和推理阶段、研究提示工程等等是提升大模型在法律行业的认知能力的有效手段。

大模型应用实例
-----
______
*LawGPT-zh*  
利用ChatGPT联想生成具体的情景问答+知识问答,使用ChatGPT基于文本构建QA对.

*Lawyer LLaMA*  
首先在大规模法律语料上进行预训练，随后借助对中国国家统一法律职业资格考试客观题的分析和对法律咨询的回答，进行指令微调。

**将大模型应用到专业领域上，微调是主要思路。而如何构建微调数据则是微调方法中的一个核心问题，在具体实践中，需要多方考虑以保证模型性能。**

[医疗AI与GPT | 梳理全球医疗大模型](https://zhuanlan.zhihu.com/p/658284168)  
[AI大模型走进医疗，如何破解落地难题？](https://zhuanlan.zhihu.com/p/673338994)  
[最新综述！预训练大模型用于医疗健康领域的全面调研](https://blog.csdn.net/amusi1994/article/details/133594022)   
[梳理中国AI法律大模型都有哪些？](https://zhuanlan.zhihu.com/p/640338124)  
[法律行业大模型交流观点整理](https://zhuanlan.zhihu.com/p/669509425)  
[解读Lawyer LLaMA，延申专业领域大模型微调：数据集构建，模型训练](https://zhuanlan.zhihu.com/p/634861170)

