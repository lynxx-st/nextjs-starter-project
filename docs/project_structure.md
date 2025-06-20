# CEO Simulator - Project Structure

## Current Structure

```
ceo-simulator/
├── docs/                           # Documentation
│   ├── architecture.md             # System architecture
│   ├── feature_tree.mmd           # Feature tree diagram
│   ├── gameplay_flowchart.mmd     # Gameplay flow
│   └── project_structure.md       # This file
├── public/                         # Static assets
│   ├── icons/                     # Game icons and images
│   └── sounds/                    # Audio files (future)
├── src/
│   ├── app/                       # Next.js app directory
│   │   ├── globals.css            # Global styles
│   │   ├── layout.tsx             # Root layout
│   │   ├── page.tsx               # Landing page
│   │   └── providers.tsx          # Context providers
│   ├── components/
│   │   ├── game/                  # Game-specific components
│   │   │   ├── CompanySetup.tsx   # Company creation form
│   │   │   ├── GameDashboard.tsx  # Main game interface
│   │   │   ├── ExecutiveTeam.tsx  # Team management (future)
│   │   │   ├── FinancialReports.tsx # Financial dashboard (future)
│   │   │   ├── StrategyPlanner.tsx # Strategic planning (future)
│   │   │   └── CrisisManager.tsx  # Crisis handling (future)
│   │   ├── ui/                    # Reusable UI components
│   │   │   ├── button.tsx         # Button component
│   │   │   ├── card.tsx           # Card component
│   │   │   ├── input.tsx          # Input component
│   │   │   ├── select.tsx         # Select component
│   │   │   └── ...                # Other shadcn/ui components
│   │   └── charts/                # Chart components (future)
│   │       ├── KPIChart.tsx       # KPI visualization
│   │       ├── FinancialChart.tsx # Financial charts
│   │       └── MarketChart.tsx    # Market analysis charts
│   ├── lib/
│   │   ├── game/                  # Game logic and state
│   │   │   ├── store.ts           # Zustand game store
│   │   │   ├── types.ts           # Game type definitions
│   │   │   ├── engine/            # Game engine modules
│   │   │   │   ├── GameEngine.ts  # Main game controller
│   │   │   │   ├── QuarterSimulator.ts # Quarter simulation
│   │   │   │   └── EventEngine.ts # Event system
│   │   │   ├── modules/           # Game modules
│   │   │   │   ├── CompanyModule.ts # Company management
│   │   │   │   ├── FinanceModule.ts # Financial calculations
│   │   │   │   ├── PeopleModule.ts # HR management
│   │   │   │   ├── OperationsModule.ts # Operations
│   │   │   │   ├── MarketModule.ts # Market dynamics
│   │   │   │   └── AnalyticsModule.ts # Analytics
│   │   │   └── ai/                # AI systems
│   │   │       ├── CompetitorAI.ts # AI competitors
│   │   │       ├── AdvisorAI.ts   # AI advisors
│   │   │       └── MarketAI.ts    # Market AI
│   │   ├── api/                   # API utilities (future)
│   │   │   ├── client.ts          # API client
│   │   │   └── types.ts           # API types
│   │   └── utils.ts               # Utility functions
│   └── hooks/                     # Custom React hooks
│       ├── use-mobile.ts          # Mobile detection
│       ├── useGameState.ts        # Game state hook (future)
│       └── useAnalytics.ts        # Analytics hook (future)
├── tests/                         # Test files (future)
│   ├── components/                # Component tests
│   ├── lib/                       # Logic tests
│   └── e2e/                       # End-to-end tests
├── .github/                       # GitHub workflows
│   └── workflows/
│       ├── ci.yml                 # Continuous integration
│       └── deploy.yml             # Deployment workflow
├── docker/                        # Docker configuration (future)
│   ├── Dockerfile                 # Frontend container
│   ├── docker-compose.yml         # Development setup
│   └── docker-compose.prod.yml    # Production setup
├── package.json                   # Dependencies and scripts
├── tsconfig.json                  # TypeScript configuration
├── tailwind.config.js             # Tailwind CSS configuration
├── next.config.ts                 # Next.js configuration
└── README.md                      # Project documentation
```

## Implementation Phases

### Phase 1: Core Foundation ✅
- [x] Project setup with Next.js and TypeScript
- [x] Basic UI components (shadcn/ui)
- [x] Company setup flow
- [x] Basic game state management
- [x] Simple dashboard interface

### Phase 2: Game Engine (In Progress)
- [ ] Quarter simulation system
- [ ] Financial calculations engine
- [ ] Basic KPI tracking
- [ ] Event system foundation
- [ ] Enhanced dashboard with real data

### Phase 3: Advanced Features
- [ ] Executive team management
- [ ] AI competitor system
- [ ] Crisis and event handling
- [ ] Advanced analytics dashboard
- [ ] Strategic planning tools

### Phase 4: Polish & Scale
- [ ] Real-time multiplayer features
- [ ] Advanced AI advisors
- [ ] Comprehensive testing suite
- [ ] Performance optimization
- [ ] Production deployment

## File Naming Conventions

### Components
- PascalCase for component files: `CompanySetup.tsx`
- Descriptive names indicating purpose
- Group related components in folders

### Utilities and Logic
- camelCase for utility files: `gameEngine.ts`
- Descriptive names for modules: `FinanceModule.ts`
- Clear separation of concerns

### Types and Interfaces
- PascalCase for type definitions
- Descriptive names: `GameState`, `CompanyMetrics`
- Group related types in dedicated files

## Development Guidelines

### Code Organization
1. Keep components focused and single-purpose
2. Extract business logic into separate modules
3. Use TypeScript for type safety
4. Follow React best practices

### State Management
1. Use Zustand for game state
2. Keep state normalized and flat
3. Use selectors for derived data
4. Implement proper state persistence

### Testing Strategy
1. Unit tests for business logic
2. Component tests for UI
3. Integration tests for workflows
4. E2E tests for critical paths
