# .NET Modernization Analyzer Power

A Kiro Power that provides enterprise-grade .NET codebase modernization analysis, generating comprehensive feasibility reports with visual architecture diagrams, proprietary dependency analysis, database migration opportunities, and strategic alignment recommendations.

## Features

- Comprehensive evaluation across 18+ modernization areas
- Visual architecture diagrams using Mermaid.js (7+ diagram types)
- Proprietary/commercial dependency impact analysis with code migration examples
- Database detection and SQL Server → Aurora PostgreSQL migration recommendations
- Migration Strategy Bank with proven patterns
- Strategic alignment with AWS 7 Rs and Gartner TIME frameworks
- "Impact If Not Modernized" risk assessments for every finding
- 3 ranked migration pathways by approachability
- Cost-benefit analysis with qualitative assessments (Low/Medium/High/Very High)
- Incremental codebase scanning for large projects (context-aware)

## Key Capabilities

### Modernization Evaluation Areas

- Platform & Framework (target version, Windows-only dependencies)
- Architecture (monolithic vs modular, layering violations)
- Dependencies (proprietary library compatibility, NuGet CVEs, license blocks)
- Code Quality (cyclomatic complexity, maintainability)
- Design Patterns (DI usage vs Service Locator)
- Data Layer (ORM type, stored procedures, N+1 queries)
- Performance (async/await usage, caching strategies)
- Testing (coverage, integration tests)
- Security (auth patterns)
- UI Layer (WinForms/WebForms vs modern frameworks)
- DevOps (CI/CD maturity, container readiness)
- Observability (structured logging, tracing)
- Documentation quality
- Business Logic (domain isolation)
- Infrastructure (on-premises vs cloud-native)
- Skills/Org (code complexity vs team capability)
- Support Lifecycle (EOL status)
- Legacy Antipatterns (global state, ThreadPool exhaustion)

### Database Detection & Migration (Critical Feature)

The power automatically scans for database technology and prominently recommends cost optimization opportunities:

- Detects SQL Server indicators (connection strings, SqlClient, T-SQL patterns)
- Identifies stored procedures and SQL Server-specific features
- Recommends SQL Server → Aurora PostgreSQL migration path
- Provides T-SQL to PostgreSQL conversion examples
- Highlights database licensing as primary cost driver
- References AWS SCT and DMS migration tools

### Cost-Benefit Analysis

Uses qualitative terms for flexibility:

- Cost levels: Low / Medium / High / Very High
- Savings potential: Low / Medium / High / Very High
- Effort complexity: Low / Medium / High
- No specific dollar amounts or timeframes

## Installation

1. Open Kiro IDE
2. Go to the Powers panel
3. Click "Install from GitHub"
4. Enter this repository URL

Or manually copy the `dotnet-modernization-analyzer` folder to your `.kiro/powers/` directory.

## Usage

Activate the power by mentioning any of these phrases:

- "analyze this .NET codebase"
- "modernization assessment"
- "migration feasibility"
- "legacy .NET application"
- "AWS migration for .NET"
- "containerize .NET app"
- "modernize to .NET Core/.NET 8"
- "evaluate modernization pathways"
- "proprietary dependency analysis"

### Example

```
User: analyze this codebase and generate me its modernization report
```

The power will automatically:

1. Scan codebase structure (incrementally for large codebases)
2. Detect database technology and connection patterns
3. Evaluate all modernization areas
4. Identify proprietary dependencies with migration examples
5. Generate visual architecture diagrams (Mermaid.js)
6. Assess SQL Server → PostgreSQL migration opportunity
7. Create `MODERNIZATION_REPORT.md` with pathways and recommendations

## Output Structure

The generated `MODERNIZATION_REPORT.md` includes:

1. **Executive Summary**
2. **Visual Architecture State**
3. **Critical Findings Matrix**
4. **Proprietary Dependency Analysis**
5. **Database Analysis & Migration Opportunity**
6. **Recommended Pathways**
7. **Next Steps**
8. **Cost-Benefit Analysis**

## Requirements

- Kiro IDE
- Access to a .NET codebase (local or repository)

## License

MIT
