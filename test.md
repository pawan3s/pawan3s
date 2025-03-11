flowchart TB
    A([Start]) --> B{Select Login Method<br>(Account-Based?)}
    B -- Yes --> C[Enter Username & Password]
    B -- No --> D[Face Login Interface]

    D --> E[Capture or Upload Face Image]
    E --> F{Is Face Verification<br>Successful?}
    F -- Yes --> G[Enter Monitoring Interface<br>Turn On Camera]
    F -- No --> D

    C --> G

    G --> H{Is an Unfamiliar<br>Face Detected?}
    H -- Yes --> I[Generate Security Alert<br>(Click for Details)]
    I --> J{Enable Security Alert,<br>Trajectory Detection,<br>or Heatmap?}
    J -- Yes --> K[Activate Selected Features]
    J -- No --> L[Skip Additional Features]
    K --> M[Update Monitoring<br>Statistics & Charts]
    L --> M
    H -- No --> M

    M --> N{Proceed to Face<br>Registration?}
    N -- Yes --> O[Display Email &<br>Face Database]
    O --> P{Register Face?}
    P -- Yes --> Q[Store Face in Database]
    P -- No --> R[Skip Registration]
    Q --> S([End])
    R --> S([End])
    N -- No --> S([End])

