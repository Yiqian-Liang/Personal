flowchart TD
  %% Supervisors
  subgraph Supervisors [Supervisors (optional)]
    direction TB
    SUP["\"Please conduct research on xxx?\"<br/>\"Can you come up with some research ideas about xxx?\""]
  end

  %% Main workflow
  subgraph MainFlow [Autonomous Generalist Scientist]
    direction LR
    A[Idea Creation<br/>• Trend Identification<br/>• Research Questions & Hypotheses<br/>• Cross-modal Brainstorming]
    B[Literature Review<br/>• Paper Search & Download<br/>• Chart/Table Interpretation<br/>• Knowledge Synthesis & Conflict Resolution]
    C[Method Design<br/>• Algorithm/Model Planning<br/>• Protocols/Equations/Code<br/>• Experimental Timeline]
    D[Experiment & Analysis<br/>• Experiment Execution & Data Collection<br/>• Data Cleaning & Feature Extraction<br/>• Results Analysis & Visualization]
    E[Writing & Reporting<br/>• Draft Generation & Citation Management<br/>• Figure & Code Snippet Integration<br/>• Peer Review & Submission]

    A --> B
    B --> C
    C --> D
    D --> E
  end

  %% Feedback loops from supervisors
  SUP -. N times .-> A
  SUP -. N times .-> B
  SUP -. N times .-> C
  SUP -. N times .-> D
  SUP -. N times .-> E

  %% Reflection loop
  E -- Reflection --> A

  %% Bottom modules
  subgraph Modules [Multi-modal Agent Capabilities]
    direction LR
    P[Perception]
    R[Reasoning]
    M[Memory]
    Ac[Action]
    O[Orchestration]
  end