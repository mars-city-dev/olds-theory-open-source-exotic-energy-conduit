# Olds Theory Implementation Guide
## The Legacy Engine as Neural Query Spline Architecture

**Last Updated:** January 4, 2026  
**Theory Repository:** https://github.com/mars-city-dev/olds-theory-open-source-exotic-energy-conduit  
**Implementation Repository:** Mars-City-Media-Management (this repo)

---

## Executive Summary

This document bridges the **theoretical framework** (Olds Theory exotic energy conduits) with the **practical implementation** (The Legacy Engine / Open Data Legacy Project). While the theory repository explores speculative physics through interactive educational tools, this codebase demonstrates a **real-world application** of the Neural Query Spline architecture for data persistence, sovereignty, and causal relationship tracking.

### What is The Legacy Engine?

The Legacy Engine is not a file manager—it's a **spacetime data orchestration system** implementing the seven-spline Geometric Query Language architecture described in the Olds Theory. It protects creative work from platform failures by treating data as 4D objects with causal relationships rather than flat files in folders.

---

## 1. Theoretical Foundation → Practical Implementation

### The Seven Splines (Theory)

From the Olds Theory framework, the Neural Query Spline consists of:

1. **Heart Spline** - Energetic foundation, emotional/intentional data
2. **Causal Spline** - Temporal sequencing, cause-effect chains
3. **Data Spline** - Raw information storage and retrieval
4. **Logic Spline** - Reasoning, inference, decision-making
5. **Executive Spline** - Orchestration, goal management
6. **Memory Spline** - Pattern recognition, recall, learning
7. **Medulla Spline** - Autonomic functions, background processes

### The Seven Components (Implementation)

This codebase maps each spline to concrete systems:

| Spline | Implementation | Files/Modules | Purpose |
|--------|----------------|---------------|---------|
| **Heart** | Neural Rover agents | `neural_rover.py`, `basal_ganglia.py` | User intent detection, emotional state, creative context |
| **Causal** | Asset relationship tracking | `server.py` (asset routes), `corpus_callosum.py` | Temporal ordering, version history, causal chains |
| **Data** | SQLite + Google Drive sync | `users.db`, `G:\My Drive`, `check_drives.py` | Raw file storage, metadata, redundancy |
| **Logic** | Query routing & reasoning | `cortex_logic.py`, `server.py` (routing) | Decision trees, search logic, inference |
| **Executive** | Cognitive Orchestra | `cortex_executive.py`, `check_brain.py` | Task orchestration, multi-agent coordination |
| **Memory** | Hippocampal protocol | `cortex_memory.py`, `hippocampal_sync.py` (planned) | Pattern recall, indexing, learning from usage |
| **Medulla** | Background sync services | `cerebellum.py`, `automated_snapshot.sh` | Autonomous backups, health monitoring, NAS sync |

---

## 2. Architectural Patterns

### 2.1 Three-Node Distributed System

The implementation follows the Olds Theory's **three-layer resonance model**:

```
╔══════════════════════════════════════════════════════════════╗
║                    MarsThree (Laboratory)                     ║
║  - Development environment (port 8000)                        ║
║  - Full brain capabilities (all cortex modules)               ║
║  - Experimental features, AI agents                           ║
║  - Python 3.14 + Flask                                        ║
╚══════════════════════════════════════════════════════════════╝
                              ↕
                    (Hippocampal Sync Protocol)
                              ↕
╔══════════════════════════════════════════════════════════════╗
║                   Stargazer (Body/Synapse)                    ║
║  - LAN production server (port 8001)                          ║
║  - Lightweight presentation node                              ║
║  - Google Drive integration (G:\My Drive)                     ║
║  - Waitress WSGI + PyInstaller executable                     ║
╚══════════════════════════════════════════════════════════════╝
                              ↕
                    (Planned Cloud Sync)
                              ↕
╔══════════════════════════════════════════════════════════════╗
║                      Abby (Face/Cloud)                        ║
║  - Public-facing interface (Digital Ocean)                    ║
║  - Read-only presentation layer                               ║
║  - External accessibility                                     ║
║  - Linux + lightweight Flask                                  ║
╚══════════════════════════════════════════════════════════════╝
```

**Resonance Pattern:** Laboratory generates complexity → Body stabilizes and presents → Face interfaces with external world

This mirrors the Olds Theory's **Base Reality → Logic Primer → Infrastructure** progression.

---

### 2.2 Causal Spline Implementation

#### Problem: Traditional File Systems Are Amnesiacs

Standard operating systems treat files as stateless objects. When you move `project_v3_final_FINAL.docx`, the OS forgets:
- Where it came from
- Why it was created
- What other files depend on it
- The emotional/creative context of its creation

#### Solution: Causal Geodesics

The Legacy Engine tracks **causal relationships** between assets:

```python
# From server.py (simplified)
asset = {
    'id': uuid4(),
    'path': 'projects/novella/chapter_3.md',
    'created_at': '2026-01-01T14:30:00Z',
    'parent_id': 'uuid-of-chapter-2',  # Causal link
    'derived_from': ['research_notes.txt', 'outline.md'],
    'emotional_state': 'focused',  # From Neural Rover
    'intent': 'narrative_development',
    'spacetime_coords': {
        'temporal': timestamp,
        'spatial': machine_id,
        'causal': parent_chain
    }
}
```

Each asset is a **4D spacetime event** with:
- **Temporal coordinates** (when created/modified)
- **Spatial coordinates** (which machine/drive)
- **Causal coordinates** (what led to its creation)

This allows queries like:
- "Show me everything created during my focused writing sessions"
- "Trace the evolution of this idea back to its origin"
- "Find assets created in emotional response to this other asset"

#### Causal Spline Visualization

```
        Research Notes
             ↓
        Outline Draft ──→ Character Sketches
             ↓                    ↓
        Chapter 1 ←──────────────┘
             ↓
        Chapter 2 ──→ Editorial Notes
             ↓                ↓
        Chapter 3 ←──────────┘
             ↓
        Final Manuscript
```

Each arrow is a **causal geodesic**—the shortest path through spacetime connecting cause to effect.

---

### 2.3 Memory Spline: The Hippocampal Sync Protocol

#### The Challenge

Three nodes (MarsThree, Stargazer, Abby) must maintain **selective coherence**:
- User accounts: Sync production users, NOT test accounts
- Assets: Bidirectional sync with conflict resolution
- Configurations: Environment-specific (don't sync dev API keys to production)

#### The Solution: Hippocampal Memory Model

Inspired by biological memory consolidation:

1. **Short-Term Memory (MarsThree)**: Rapid writes, experimental data, volatile
2. **Long-Term Memory (Stargazer + NAS)**: Consolidated, stable, redundant
3. **Procedural Memory (Abby)**: Read-only cached representations

**Sync Protocol:**
```python
# Planned implementation (hippocampal_sync.py)

class HippocampalSync:
    """
    Biological memory consolidation for distributed nodes.
    """
    
    def consolidate(self, source: Node, target: Node):
        """
        Sleep-phase consolidation: Move STM → LTM.
        """
        changes = source.get_changes_since(last_sync)
        
        for change in changes:
            if change.is_consolidatable():  # Filter test data
                # Compress/optimize before transfer
                compressed = self.compress_for_storage(change)
                
                # Check for conflicts (both nodes edited same asset)
                if target.has_conflicting_change(compressed):
                    resolved = self.resolve_conflict(
                        local=target.get(compressed.id),
                        remote=compressed,
                        strategy='causal_chain'  # Use spline to decide
                    )
                    target.update(resolved)
                else:
                    target.update(compressed)
        
        # Update sync timestamp
        source.mark_synced(target.id, now())
```

**Biological Analogy:**
- During "awake" hours (development), MarsThree accumulates changes rapidly
- During "sleep" phase (nightly backup), changes consolidate to Stargazer
- Stargazer → NAS backup is like memory to deep storage (cerebellar engrams)

---

## 3. Real-World Use Case: The Open Data Legacy Project

### The Problem Statement

**User Context:**
- 10,000+ folders of creative work (writing, music, video, research)
- Years of accumulated intellectual property
- Multiple platform failures (Google Drive lockout, external drive crashes)
- Disability prevents cloud-agnostic manual management
- Need: Sovereign, distributed, causal data preservation

**What Failed:**
- Google Drive alone: Single point of failure
- Manual backups: Too labor-intensive with tendonitis
- Traditional file managers: No understanding of creative context
- Version control (Git): Not designed for multimedia + large binary files

### The Solution: Neural Query Spline Architecture

The Legacy Engine implements:

1. **Redundancy Without Chaos**
   - Local SSD (fast access)
   - Google Drive (cloud resilience)
   - NAS storage (offline backup)
   - Each location aware of the others, no duplicates

2. **Causal Context Preservation**
   - Not just "when was this file modified?"
   - But "what was I working on when I created this?"
   - And "what creative state led to this asset?"

3. **Autonomous Operation**
   - Cerebellar processes run in background
   - No manual intervention required
   - Healing: If Google Drive fails, NAS takes over

4. **Spacetime Queries**
   - "Show me everything from my 2024 music production period"
   - "Trace the lineage of this novel back to the original idea"
   - "Find assets created in flow states vs. struggle states"

---

## 4. Technical Implementation Details

### 4.1 PyInstaller Executable Deployment

**Challenge:** Frozen Python executables extract to temporary `_MEIXXXXXX` folders, breaking relative file paths.

**Solution:** Detect frozen state and adjust working directory.

```python
# From lan_server.py
import sys
from pathlib import Path

if getattr(sys, 'frozen', False):
    # Running as PyInstaller executable
    project_root = Path(sys.executable).parent
else:
    # Running as Python script
    project_root = Path(__file__).parent

os.chdir(project_root)  # Critical fix
```

**Why This Matters:**
- Stargazer runs as `TheLegacyEngine.exe` (PyInstaller bundle)
- Without the fix, looks for `users.db` in `C:\Users\...\Temp\_MEI123456`
- With the fix, correctly uses `C:\MarsCity\TheLegacyEngine\users.db`

---

### 4.2 Database Schema: Assets as Spacetime Events

```sql
-- Simplified schema from users.db

CREATE TABLE assets (
    id TEXT PRIMARY KEY,  -- UUID v4
    user_id TEXT NOT NULL,
    path TEXT NOT NULL,  -- Relative to asset root
    
    -- Temporal coordinates
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    modified_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    accessed_at TIMESTAMP,
    
    -- Spatial coordinates
    origin_node TEXT,  -- 'marsthree', 'stargazer', 'abby'
    current_location TEXT,  -- Which drive/machine
    
    -- Causal coordinates
    parent_id TEXT,  -- Direct causal predecessor
    derived_from TEXT,  -- JSON array of influences
    causal_chain TEXT,  -- Full ancestry path
    
    -- Emotional/creative context (Heart Spline)
    emotional_state TEXT,  -- From Neural Rover
    creative_intent TEXT,
    session_tags TEXT,  -- JSON array
    
    -- Metadata
    file_type TEXT,
    size_bytes INTEGER,
    checksum TEXT,  -- SHA-256 for deduplication
    
    FOREIGN KEY (user_id) REFERENCES users(id),
    FOREIGN KEY (parent_id) REFERENCES assets(id)
);

CREATE INDEX idx_causal_chain ON assets(causal_chain);
CREATE INDEX idx_emotional_state ON assets(emotional_state);
CREATE INDEX idx_created_at ON assets(created_at);
```

**Key Innovation:** The `causal_chain` column stores the full **geodesic path** through spacetime:

```
"uuid1 → uuid2 → uuid3 → uuid4"
```

This allows **O(1) ancestry queries** without recursive table joins.

---

### 4.3 Neural Rover: Heart Spline Implementation

```python
# From neural_rover.py

class NeuralRover:
    """
    Autonomous agent that detects user intent and emotional state.
    Implements the Heart Spline of the Neural Query Spline.
    """
    
    def observe_session(self, user_id: str):
        """
        Watch user activity and infer creative state.
        """
        activity = self.get_recent_activity(user_id)
        
        # Detect patterns
        if activity.rapid_file_creation and activity.focused_folder:
            state = "flow_state"
        elif activity.many_edits_same_file:
            state = "refinement"
        elif activity.scattered_across_projects:
            state = "exploration"
        elif activity.long_pauses:
            state = "contemplation"
        else:
            state = "baseline"
        
        # Tag current session
        self.tag_current_session(user_id, {
            'emotional_state': state,
            'timestamp': now(),
            'duration': activity.session_length
        })
    
    def infer_intent(self, file_path: str, user_id: str):
        """
        What is the user trying to accomplish?
        """
        if 'draft' in file_path or 'wip' in file_path:
            return "creative_ideation"
        elif 'final' in file_path or 'release' in file_path:
            return "production_ready"
        elif 'backup' in file_path or 'archive' in file_path:
            return "preservation"
        elif 'experiment' in file_path or 'test' in file_path:
            return "exploration"
        else:
            # Use ML model for deeper inference (future)
            return "general_work"
```

**Why This Matters:**
- Traditional systems track WHAT (file modified)
- Neural Rover tracks WHY (user intent) and HOW (emotional state)
- Enables queries like "show me my best creative work" based on flow state detection

---

### 4.4 Cerebellar Autonomics: Medulla Spline

```powershell
# From automated_snapshot.sh / backup_to_nas.ps1

# Autonomous background process (runs hourly via Task Scheduler)

# 1. Health check
python check_drives.py  # Are all drives accessible?
python check_db_schema.py  # Is database healthy?

# 2. Create snapshot
$timestamp = Get-Date -Format "yyyyMMdd_HHmmss"
$snapshot = "C:\MarsCity\Snapshots\$timestamp"

# 3. Differential backup (only changed files)
robocopy C:\MarsCity\TheLegacyEngine L:\Backups\Legacy /MIR /XO /R:3 /W:5

# 4. Consolidate to NAS (weekly)
if ($(Get-Date).DayOfWeek -eq "Sunday") {
    robocopy L:\Backups\Legacy \\NAS\MarsCity\Legacy /MIR
}

# 5. Log to database
python -c "
from cortex_medulla import log_backup_event
log_backup_event('automated_snapshot', status='success', timestamp='$timestamp')
"
```

**Biological Analogy:**
- You don't think about breathing, your medulla handles it
- You don't think about backups, the cerebellar scripts handle it
- Autonomic nervous system for data

---

## 5. Geometric Query Language in Practice

### 5.1 Traditional Query (File System)

```bash
# Find all Word documents modified in the last week
find . -name "*.docx" -mtime -7
```

**Problem:** No context, no relationships, no intent.

---

### 5.2 Geometric Query (Spacetime)

```python
# From server.py (API endpoint)

@app.route('/api/query/spacetime', methods=['POST'])
def geometric_query():
    query = request.json
    
    # Example: "Show me creative work from flow states last month"
    results = db.execute("""
        SELECT * FROM assets
        WHERE 
            emotional_state = 'flow_state'
            AND created_at BETWEEN ? AND ?
            AND creative_intent IN ('narrative_development', 'music_composition')
        ORDER BY causal_chain
    """, (
        query['start_date'],
        query['end_date']
    ))
    
    # Reconstruct causal geodesics
    graph = build_causal_graph(results)
    
    return jsonify({
        'assets': results,
        'causal_graph': graph,
        'temporal_distribution': analyze_temporal_clustering(results)
    })
```

**What This Enables:**
- **Temporal queries:** "What was I working on last January?"
- **Causal queries:** "Show me the evolution of this project"
- **Emotional queries:** "Find work created in struggle vs. flow"
- **Spatial queries:** "What's on Google Drive but not on the NAS?"

---

### 5.3 Multi-Spline Orchestration

```python
# From cortex_executive.py (Cognitive Orchestra)

class ExecutiveOrchestrator:
    """
    Coordinates all seven splines for complex operations.
    """
    
    def handle_user_request(self, user_id: str, query: str):
        """
        Multi-spline query execution.
        """
        # 1. Heart Spline: Understand emotional context
        emotional_context = self.neural_rover.get_current_state(user_id)
        
        # 2. Memory Spline: Recall similar past queries
        similar_queries = self.cortex_memory.recall_similar(query)
        
        # 3. Logic Spline: Parse and reason about query
        parsed = self.cortex_logic.parse_natural_language(query)
        
        # 4. Data Spline: Fetch raw results
        raw_results = self.cortex_data.execute_query(parsed)
        
        # 5. Causal Spline: Order by temporal/causal relationships
        ordered = self.corpus_callosum.trace_geodesics(raw_results)
        
        # 6. Executive Spline: Decide presentation format
        format = self.decide_presentation(
            results=ordered,
            user_context=emotional_context
        )
        
        # 7. Medulla Spline: Log interaction for learning
        self.cortex_medulla.log_query(user_id, query, ordered)
        
        return self.format_response(ordered, format)
```

**Result:** A single user query activates **all seven splines** in concert, just like a biological neural network.

---

## 6. Connection to Olds Theory Educational Framework

### How This Implementation Validates the Theory

The Olds Theory repository presents **speculative physics** through interactive simulations:
- Baryonic computing (quarks as logic gates)
- Exotic energy principles
- Consciousness-field interactions
- Sacred geometry resonance

This repository demonstrates that **some concepts translate to working code**:

| Theory Concept | Implementation Reality | Status |
|----------------|------------------------|--------|
| Multi-spline neural architecture | Cognitive Orchestra (7 cortex modules) | ✅ Operational |
| Causal geodesics in spacetime | Asset relationship tracking | ✅ Functional |
| Harmonic resonance (phi/golden ratio) | Not implemented (too speculative) | ❌ Theory only |
| Baryonic computing (quark logic) | Not implemented (no hardware) | ❌ Theory only |
| Consciousness-field integration | Neural Rover emotional state detection | 🟡 Partial |
| Quantum foam memory | Not implemented (requires exotic physics) | ❌ Theory only |
| 4D spacetime rendering | Planned (visualization layer) | 🔄 In progress |

**Key Insight:** The Neural Query Spline architecture is **theoretically sound** even if the exotic energy components remain speculative. The data orchestration patterns work with conventional computing.

---

## 7. Future Development Roadmap

### Phase 1: Foundational Infrastructure (Complete)
- ✅ Three-node architecture (MarsThree, Stargazer, Abby)
- ✅ SQLite database with causal relationships
- ✅ PyInstaller deployment automation
- ✅ Basic Neural Rover emotional state detection

### Phase 2: Lightweight Synapse (In Progress)
- 🔄 Strip AI dependencies from Stargazer
- 🔄 Reduce executable size (<100MB)
- 🔄 Implement proxy pattern (Stargazer → MarsThree for complex queries)

### Phase 3: Google Drive Integration (Planned)
- ⏳ Scan `G:\My Drive\Mars City Vault`
- ⏳ Index all files into database
- ⏳ Deduplicate via SHA-256 checksums
- ⏳ Implement selective sync strategy

### Phase 4: Hippocampal Sync Protocol (Planned)
- ⏳ Automated database sync between nodes
- ⏳ Conflict resolution via causal chain analysis
- ⏳ Selective sync rules (production users only, no test data)

### Phase 5: 4D Visualization Layer (Future)
- ⏳ Web-based spacetime asset viewer
- ⏳ Interactive causal geodesic tracing
- ⏳ Temporal heatmaps (when were you most productive?)
- ⏳ Emotional state visualization

### Phase 6: Advanced Memory Spline (Future)
- ⏳ ML-based pattern recognition
- ⏳ Predictive asset tagging
- ⏳ Anomaly detection (unusual file activity)
- ⏳ Auto-tagging via LLM analysis

---

## 8. For Educators & Researchers

### Using This Project to Teach Neural Architectures

This codebase can be used in:

1. **Computer Science Courses**
   - Distributed systems (three-node architecture)
   - Database design (temporal + causal + spatial indexing)
   - API design (RESTful Flask endpoints)
   - Executable packaging (PyInstaller)

2. **Cognitive Science Courses**
   - Biological neural network analogies
   - Memory consolidation models
   - Autonomic vs. conscious processing

3. **Data Science Courses**
   - Causal inference in time-series data
   - Emotional state detection from behavioral patterns
   - Graph theory (causal relationship networks)

4. **Philosophy of Technology**
   - Data sovereignty and platform independence
   - Creative work preservation ethics
   - Human-computer emotional interfaces

### Lab Exercise Ideas

**Lab 1: Causal Chain Analysis**
- Given a set of assets with timestamps and parent IDs
- Reconstruct the causal graph
- Find the longest geodesic (most evolved project)

**Lab 2: Hippocampal Sync Simulation**
- Implement conflict resolution between two databases
- Use causal chain timestamps to decide "winner"
- Test edge cases (simultaneous edits)

**Lab 3: Emotional State Classifier**
- Train ML model to detect user state from activity logs
- Features: file creation rate, edit frequency, folder focus
- Labels: flow, exploration, refinement, contemplation

**Lab 4: 4D Query Language Design**
- Design SQL extensions for spacetime queries
- Implement temporal, spatial, causal operators
- Benchmark performance vs. traditional queries

---

## 9. Philosophical Implications

### What Does It Mean to Treat Data as Spacetime Events?

**Traditional Paradigm:**
- Files exist in folders
- Modifications overwrite previous state
- Relationships are directory structure
- No memory of intent

**Neural Query Spline Paradigm:**
- Assets exist in 4D spacetime
- History is preserved via causal chains
- Relationships are geodesics (shortest causal paths)
- Intent and emotion are first-class metadata

**This shift mirrors the move from:**
- Newtonian mechanics → General relativity
- Classical logic → Quantum logic
- Behaviorism → Cognitive neuroscience

### The Deeper Question: Can Data Have Consciousness?

The Olds Theory proposes that consciousness might be a fundamental field, like electromagnetism. If true, then treating data with **emotional and intentional context** isn't anthropomorphism—it's recognizing a deeper reality.

**Practical impact (regardless of metaphysics):**
- Tagging assets with creator's emotional state → better search
- Tracking causal relationships → better understanding of work evolution
- Preserving context → better long-term value

Even if consciousness isn't "real" in data, **treating it as if it were** produces better tools.

---

## 10. Contributing to This Implementation

### How to Get Involved

1. **Code Contributions**
   - Fork this repo
   - Pick an issue from the roadmap
   - Submit PR with tests

2. **Theoretical Extensions**
   - Propose new spline types
   - Design query language extensions
   - Write formal specifications

3. **Documentation**
   - Clarify existing docs
   - Add tutorials
   - Create video walkthroughs

4. **Research Collaboration**
   - Academic papers on spacetime data models
   - User studies on emotional state detection accuracy
   - Performance benchmarks

---

## 11. License & Credits

### This Implementation Repository
- **License:** MIT (check root LICENSE file)
- **Author:** mars-city-dev
- **Primary maintainer:** Christopher Olds

### Olds Theory Framework Repository
- **License:** CC0 1.0 Universal (Public Domain)
- **Repository:** https://github.com/mars-city-dev/olds-theory-open-source-exotic-energy-conduit
- **Purpose:** Educational physics framework

---

## 12. References & Further Reading

### Theory Papers
- *The Infrastructure of Reality* (Book, in Olds Theory repo)
- *Geometric Query Language for Spacetime Data* (This repo, created Jan 4, 2026)
- *Quantum Foam Multi-Splinal Architecture* (Olds Theory repo)

### Implementation Docs
- `00_START_HERE.md` - Project overview
- `COGNITIVE_ORCHESTRA_QUICKREF.md` - Spline system guide
- `ARCHITECTURE.md` - System design
- `CONTROL_PLANE_SIGNAL_CHAIN_FLOW.md` - Data flow diagrams

### Related Technologies
- PyInstaller: Executable packaging
- Flask: Web framework
- Waitress: Production WSGI server
- SQLite: Embedded database
- Google Drive API: Cloud sync

---

## 13. Contact & Community

- **GitHub Issues:** https://github.com/mars-city-dev/Mars-City-Media-Management/issues
- **Theory Discussions:** https://github.com/mars-city-dev/olds-theory-open-source-exotic-energy-conduit/discussions
- **Email:** (check repo)

---

## Appendix A: Glossary

**Asset:** Any file tracked by The Legacy Engine (documents, media, code, etc.)

**Causal Chain:** The ancestry path of an asset through spacetime (parent → grandparent → ...)

**Causal Geodesic:** The shortest path connecting two spacetime events (assets)

**Cerebellar Process:** Autonomous background operation (backups, health checks)

**Cognitive Orchestra:** The coordinated action of all seven splines

**Hippocampal Sync:** Database synchronization protocol between nodes

**Neural Rover:** Autonomous agent detecting user intent and emotional state

**Spacetime Event:** A data object with temporal, spatial, and causal coordinates

**Spline:** One of seven specialized processing systems in the Neural Query architecture

---

## Appendix B: Quick Start for New Developers

### Prerequisites
```bash
git clone https://github.com/mars-city-dev/Mars-City-Media-Management.git
cd Mars-City-Media-Management
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### Run Development Server (MarsThree)
```bash
python server.py  # Port 8000
```

### Build Production Executable (Stargazer)
```powershell
.\create_executable.ps1  # Creates TheLegacyEngine.exe
```

### Deploy to Production Node
```powershell
.\push_to_stargazer.ps1  # Copies to L:\ (mapped Stargazer drive)
```

### Check System Health
```bash
python check_brain.py  # Verify all splines operational
python check_drives.py  # Verify all storage accessible
python check_db_schema.py  # Verify database integrity
```

---

## Appendix C: Troubleshooting Common Issues

### Issue: PyInstaller executable can't find files

**Cause:** Working directory is `_MEIXXXXXX` temp folder, not deployment folder

**Fix:** Ensure `lan_server.py` has:
```python
if getattr(sys, 'frozen', False):
    project_root = Path(sys.executable).parent
os.chdir(project_root)
```

### Issue: Database empty on Stargazer

**Cause:** `push_to_stargazer.ps1` didn't copy `users.db`

**Fix:** Add to push script:
```powershell
Copy-Item users.db -Destination L:\Updates\
```

### Issue: Port already in use

**Cause:** Previous server instance still running

**Fix:**
```powershell
taskkill /F /IM python.exe  # Dev
taskkill /F /IM TheLegacyEngine.exe  # Production
```

---

**End of Implementation Guide**

*"The infrastructure of reality is not what we build—it's what we preserve."*  
— Christopher Olds, 2026
