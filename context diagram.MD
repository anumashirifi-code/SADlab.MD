    A[Patient Management] --> B[Patient Information]
    A --> C[Appointments]
    A --> D[Medical Records]
    A --> E[Treatment]
    A --> F[Care Plan]
    
    G[Billing & Insurance Claims] --> H[Payments]
    G --> I[Invoices]
    G --> J[Insurance Policies]
    G --> K[Claims]
    
    L[Lab Test Diagnostics] --> M[Test Requests]
    L --> N[Samples]
    L --> O[Test Processing]
    L --> P[Results]
    
    A -.->|shares data| G
    A -.->|orders tests| L
    L -.->|results to| A
    G -.->|claims from| L
    
    style A stroke:#818cf8,fill:#eef2ff
    style G stroke:#2dd4bf,fill:#f0fdfa
    style L stroke:#a78bfa,fill:#f5f3ff
    style B stroke:#818cf8,fill:#eef2ff
    style C stroke:#818cf8,fill:#eef2ff
    style D stroke:#818cf8,fill:#eef2ff
    style E stroke:#818cf8,fill:#eef2ff
    style F stroke:#818cf8,fill:#eef2ff
    style H stroke:#2dd4bf,fill:#f0fdfa
    style I stroke:#2dd4bf,fill:#f0fdfa
    style J stroke:#2dd4bf,fill:#f0fdfa
    style K stroke:#2dd4bf,fill:#f0fdfa
    style M stroke:#a78bfa,fill:#f5f3ff
    style N stroke:#a78bfa,fill:#f5f3ff
    style O stroke:#a78bfa,fill:#f5f3ff
    style P stroke:#a78bfa,fill:#f5f3ff
