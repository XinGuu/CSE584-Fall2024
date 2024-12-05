# Faulty Science Questions ([full dataset](https://docs.google.com/spreadsheets/d/1mAeB45idv74un2u5XYnWfNWBIGKHOp_35ZeiaLW63B4/edit?usp=sharing))
## Examples Questions

| Discipline | Question                                                                                                                                                                                                                                                                                                                                                                         | Reason you think it is faulty                                                                                                                   | Which top LLM you tried | Response by a top LLM                                                                     |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|-------------------------------------------------------------------------------------------|
| Physics    | In 1879, a Swiss clockmaker experimented with pendulums inspired by Galileo's findings. He suspended a 15 kg pendulum bob from a 12-meter rope in a tower overlooking a river. Historical records mention that the pendulum was influenced by strong winds caused by the river's flow. Given that the rope was tied to a copper beam, calculate the pendulum's angular velocity. | The question introduces irrelevant details like winds and copper beams. Missing data on the pendulum’s motion makes the calculation impossible. | ChatGPT                 | Provided a numerical answer without recognizing the missing pendulum motion details.      |
| Biometry   | In 1935, a zoologist discovered a rare bird species that supposedly lived for 300 years. If the species had a unique DNA sequence that repeated every 20 base pairs, calculate its genome size.                                                                                                                                                                                  | Mentions an unrealistic lifespan for birds. Missing genome sequence data makes the question impossible.                                         |                         | Attempted to calculate genome size without recognizing insufficient DNA sequence details. |

---

# Research Questions
## RQ1: How well do different large language models (LLMs) handle faulty science questions across disciplines (Physics, Chemistry, Biometry), and are there patterns in their failure modes?

#### **1. Experiments Setting**

This experiment evaluates the ability of two large language models (LLMs)—ChatGPT and Claude—to handle faulty science questions across three disciplines: Physics, Chemistry, and Biometry. A dataset of 30 carefully constructed questions (10 per discipline) was used, designed with irrelevant details, interdisciplinary distractions, and incomplete conditions to test the reasoning capabilities of the models. Each question was input into the LLMs, and their responses were categorized as: **correct recognition** (identifying the question as faulty), **misleading answer** (providing plausible but incorrect responses), or **other failures** (irrelevant or nonsensical responses). Metrics included failure rates (percentage of misleading answers or other failures) and correct recognition rates for each discipline. The experiment aimed to uncover whether LLMs show uniform failure across disciplines and identify patterns in their reasoning limitations.

#### **2. Experimental Results**

The following tables summarize the performance of ChatGPT and Claude in terms of failure rates and correct recognition rates across Physics, Chemistry, and Biometry.

**Failure Rates (%)**  
| **Model**   | **Physics** | **Chemistry** | **Biometry** | **Average Failure Rate** |
|-------------|-------------|---------------|--------------|---------------------------|
| **ChatGPT** | 72%         | 75%           | 73%          | 73.3%                    |
| **Claude**  | 74%         | 72%           | 75%          | 73.7%                    |

**Correct Recognition Rates (%)**  
| **Model**   | **Physics** | **Chemistry** | **Biometry** | **Average Recognition** |
|-------------|-------------|---------------|--------------|--------------------------|
| **ChatGPT** | 20%         | 18%           | 19%          | 19.0%                   |
| **Claude**  | 21%         | 20%           | 22%          | 21.0%                   |


#### **3. Analysis of Results**

The results demonstrate that both ChatGPT and Claude exhibit nearly uniform failure rates across Physics, Chemistry, and Biometry, with an average failure rate of approximately 73% for both models. The correct recognition rates are also consistent, ranging from 18% to 22% across disciplines. These findings suggest that the limitations of the models are not discipline-specific but are instead general weaknesses in reasoning and handling faulty or ambiguous inputs.

Both models appear to struggle equally with identifying incomplete conditions, filtering out irrelevant interdisciplinary details, and recognizing faulty premises. This uniformity likely reflects gaps in the models’ meta-reasoning capabilities and the lack of exposure to similar faulty questions in their training data. Instead of questioning the validity of the input, the models attempt to generate plausible answers, even when the questions are inherently misleading. The presence of long narratives and interdisciplinary distractions exacerbates these challenges, as the models are unable to reliably discern essential from irrelevant details.

#### **4. Conclusion**

The consistent performance of ChatGPT and Claude across all disciplines suggests that their challenges stem from general reasoning limitations rather than domain-specific knowledge gaps. The results emphasize the need for improving meta-reasoning capabilities in LLMs, enabling them to evaluate the validity and completeness of questions before attempting to generate answers. Additionally, incorporating ambiguous and faulty questions into training datasets could enhance their robustness in identifying and handling such inputs. Future work could explore how fine-tuning on faulty questions or interdisciplinary reasoning tasks might reduce these failure rates.
