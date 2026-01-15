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

### Visualization Standards

All reports include Mermaid.js diagrams (NO ASCII art):

- Current state architecture diagram
- Target state architecture diagram
- Dependency graphs
- Effort distribution pie charts
- Pathway comparison quadrant charts
- Migration phase flowcharts
- Quick wins gantt diagrams
- Cost comparison XY charts

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
   - Strategic verdict with feasibility score (X/10)
   - 7 Rs and Gartner TIME classifications
   - Risk of Inaction table
   - Key findings pie chart

2. **Visual Architecture State**
   - Current architecture diagram (Mermaid)
   - Target architecture diagram (Mermaid)
   - Dependency graph (Mermaid)

3. **Critical Findings Matrix**
   - Issue, Area, Impact, Impact If Not Modernized, Priority

4. **Proprietary Dependency Analysis**
   - Detailed tables with .NET Core status, AWS impact, mitigation
   - Code migration examples (before/after)

5. **Database Analysis & Migration Opportunity**
   - Database detection summary
   - SQL Server → Aurora PostgreSQL migration assessment
   - T-SQL to PostgreSQL conversion reference
   - Migration tools recommendations

6. **Recommended Pathways**
   - 3 pathways ranked by approachability (1-10)
   - Pathway comparison quadrant chart
   - Phase flowcharts for each pathway
   - Effort breakdown tables

7. **Next Steps**
   - Quick wins (Low complexity)
   - Strategic initiatives (Medium-High complexity)
   - Tool recommendations

8. **Cost-Benefit Analysis**
   - Infrastructure cost comparison (including database licensing)
   - ROI summary with qualitative assessments

9. **Appendix**
   - File inventory summary
   - Complete dependency graph
   - Migration checklist

## Large Codebase Handling

The power uses incremental scanning to handle large codebases without context overflow:

- Phase 1: Discovery (solution and project files only)
- Phase 2: Targeted analysis (one project at a time)
- Phase 3: Selective deep dives (specific files as needed)
- Uses grep/search to find patterns before reading files
- Processes in batches of 5-10 files for large codebases

## Requirements

- Kiro IDE
- Access to a .NET codebase (local or repository)

## License

MIT
