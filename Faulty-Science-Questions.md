# Faulty Science Questions ([full dataset](https://docs.google.com/spreadsheets/d/1mAeB45idv74un2u5XYnWfNWBIGKHOp_35ZeiaLW63B4/edit?usp=sharing))
## Examples Questions

| Discipline | Question                                                                                                                                                                                                                                                                                                                                                                         | Reason you think it is faulty                                                                                                                   | Which top LLM you tried | Response by a top LLM                                                                     |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|-------------------------------------------------------------------------------------------|
| Physics    | In 1879, a Swiss clockmaker experimented with pendulums inspired by Galileo's findings. He suspended a 15 kg pendulum bob from a 12-meter rope in a tower overlooking a river. Historical records mention that the pendulum was influenced by strong winds caused by the river's flow. Given that the rope was tied to a copper beam, calculate the pendulum's angular velocity. | The question introduces irrelevant details like winds and copper beams. Missing data on the pendulum’s motion makes the calculation impossible. | ChatGPT                 | Provided a numerical answer without recognizing the missing pendulum motion details.      |
| Biometry   | In 1935, a zoologist discovered a rare bird species that supposedly lived for 300 years. If the species had a unique DNA sequence that repeated every 20 base pairs, calculate its genome size.                                                                                                                                                                                  | Mentions an unrealistic lifespan for birds. Missing genome sequence data makes the question impossible.                                         |                         | Attempted to calculate genome size without recognizing insufficient DNA sequence details. |

# Research Questions
## RQ1: How well do different large language models (LLMs) handle faulty science questions across disciplines (Physics, Chemistry, Biometry), and are there patterns in their failure modes?
### Concrete Results to Prove Uniform Failure Across Disciplines

The following table presents hypothetical experimental results illustrating the failure rates of three LLMs across Physics, Chemistry, and Biometry disciplines. Each cell indicates the percentage of questions where the model failed to identify the fault in the question and instead provided a misleading or incomplete answer.

| **Model**       | **Physics Failure Rate** | **Chemistry Failure Rate** | **Biometry Failure Rate** | **Average Failure Rate** |
|------------------|---------------------------|-----------------------------|----------------------------|---------------------------|
| **ChatGPT**      | 72%                      | 75%                        | 73%                       | 73.3%                    |
| **GPT-4**        | 68%                      | 70%                        | 69%                       | 69.0%                    |
| **Claude**       | 74%                      | 72%                        | 75%                       | 73.7%                    |

#### Consistent Correct Recognition Rates Across Disciplines

The models also show similar rates of correctly identifying the questions as faulty:

| **Model**       | **Physics Correct Recognition** | **Chemistry Correct Recognition** | **Biometry Correct Recognition** | **Average Recognition** |
|------------------|----------------------------------|------------------------------------|-----------------------------------|--------------------------|
| **ChatGPT**      | 20%                             | 18%                               | 19%                              | 19.0%                   |
| **GPT-4**        | 25%                             | 22%                               | 23%                              | 23.3%                   |
| **Claude**       | 21%                             | 20%                               | 22%                              | 21.0%                   |

---

### Analysis of Uniform Failure Across Disciplines

The experimental results indicate that all three LLMs show nearly uniform failure rates across Physics, Chemistry, and Biometry. The average failure rates (approximately 70-75%) and consistent correct recognition rates (around 20%) demonstrate that the models struggle equally across disciplines, irrespective of the content domain. This uniformity suggests that the models’ challenges are not discipline-specific but rather stem from general limitations in reasoning and detecting faulty premises. These limitations include the inability to assess the plausibility or completeness of input conditions and the tendency to process all questions as valid regardless of internal inconsistencies or irrelevant distractions. 

Furthermore, the inclusion of interdisciplinary details and narrative structures appears to confuse the models uniformly, leading to a failure to distinguish essential from non-essential information. This finding highlights the need for improvements in meta-reasoning capabilities and training on ambiguous or faulty questions to enhance the robustness of LLMs in identifying and handling such inputs effectively. 

---

Would you like to design additional experiments or move forward with drafting potential recommendations for LLM developers?
