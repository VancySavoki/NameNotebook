

# 🔍 NameNotebook


<p align="right">
  <a href="README_EN.md">English</a> |
  <a href="README.md">中文版</a>
</p>

<div align="center">
  <h1>NameNotebook</h1>
  <h3>A notebook that explains how to name a project or variable effectively.</h3>
</div>

## Distributed Scheduling and Orchestration Domain
In the design of **distributed systems, orchestration systems, task scheduling systems**, and other complex systems, naming is not only key to code readability but also an essential component of system architecture expression. Below is a **professional, systematic, and actionable** naming convention recommendation covering core areas such as **distributed coordination, task orchestration, resource scheduling, state management, node communication, and elastic scaling**.

---

## 🧩 I. Naming Principles (Applicable to Distributed, Orchestration, and Scheduling Domains)

| Principle | Description |
|---------|-------------|
| **Semantic Clarity** | Names should accurately express functionality or responsibilities. Avoid vague terms (e.g., `Manager`, `Handler` which lack clear meaning when used alone). |
| **Consistent Style** | Use consistent naming styles within the same module or system (e.g., `Controller`, `Coordinator`, `Scheduler`). |
| **Structured Naming** | Recommend using the `{Resource}{Action}{Role}` structure, such as `JobScheduler`, `NodeReconciler`. |
| **Domain Terminology Priority** | Use industry-standard terms like `Orchestrator`, `Scheduler`, `Reconciler`, `Controller`, `Agent`. |
| **Differentiate Synchronous & Asynchronous** | E.g., `SyncWorker` vs `AsyncWorker`, `SyncTask` vs `BackgroundTask`. |
| **Differentiate State & Behavior** | E.g., `NodeState` vs `NodeStateManager`, `JobStatus` vs `JobScheduler`. |

---

## 📌 II. Core Component Naming Recommendations (By Function)

### 1. Distributed Coordination

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Coordinator** | Distributed coordinator | `TaskCoordinator`, `ClusterCoordinator` |
| **LeaderElector** | Leader election mechanism | `ETCDLeaderElector`, `RaftLeaderElector` |
| **LockManager** | Distributed lock management | `DistributedLockManager`, `ZooKeeperLockManager` |
| **MembershipManager** | Node membership management | `ClusterMembershipManager` |
| **DiscoveryService** | Node/service discovery | `ServiceDiscovery`, `NodeDiscovery` |
| **Consensus** | Consensus algorithm | `RaftConsensus`, `PaxosConsensus` |
| **Barrier** | Distributed barrier synchronization | `DistributedBarrier`, `TaskBarrier` |
| **Registry** | Resource registration center | `ServiceRegistry`, `NodeRegistry` |

---

### 2. Orchestration Systems

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Orchestrator** | Core orchestrator | `DeploymentOrchestrator`, `WorkflowOrchestrator` |
| **Reconciler** | State reconciler (Kubernetes style) | `PodReconciler`, `StatefulSetReconciler` |
| **Controller** | Controller | `ReplicaSetController`, `DeploymentController` |
| **Planner** | Execution plan formulation | `ExecutionPlanner`, `ResourcePlanner` |
| **Dispatcher** | Task dispatcher | `TaskDispatcher`, `ActionDispatcher` |
| **Executor** | Task executor | `RemoteExecutor`, `ContainerExecutor` |
| **Agent** | Node agent | `NodeAgent`, `WorkerAgent` |
| **Worker** | Worker node | `TaskWorker`, `ExecutionWorker` |

---

### 3. Scheduling Systems

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Scheduler** | General scheduler | `JobScheduler`, `TaskScheduler` |
| **Dispatcher** | Scheduling task dispatch | `ScheduleDispatcher` |
| **PreemptionManager** | Priority preemption management | `JobPreemptionManager` |
| **QueueManager** | Scheduling queue management | `PriorityQueueManager` |
| **SchedulerPolicy** | Scheduling policy | `RoundRobinPolicy`, `LeastUsedPolicy` |
| **NodeSelector** | Node selector | `NodeSelector`, `AffinitySelector` |
| **ResourceAllocator** | Resource allocator | `CPUAllocator`, `GPUAllocator` |
| **SchedulerExtender** | Scheduler extender | `CustomSchedulerExtender` |

---

### 4. Resource Management

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **ResourceManager** | Resource management | `ClusterResourceManager`, `NodeResourceManager` |
| **ResourceMonitor** | Resource monitoring | `MemoryMonitor`, `CPUUsageMonitor` |
| **CapacityManager** | Capacity management | `NodeCapacityManager` |
| **QuotaManager** | Quota management | `TenantQuotaManager`, `ResourceQuotaManager` |
| **Allocator** | Resource allocation | `IPAllocator`, `PortAllocator` |
| **Provisioner** | Resource provisioning | `VolumeProvisioner`, `NodeProvisioner` |
| **Scaler** | Elastic scaling | `AutoScaler`, `ReplicaScaler` |

---

### 5. Tasks & Workflows

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Job** | Task unit | `BatchJob`, `CronJob` |
| **Task** | Subtask | `MapTask`, `ReduceTask` |
| **Workflow** | Workflow | `DAGWorkflow`, `SequentialWorkflow` |
| **Stage** | Workflow stage | `ExecutionStage`, `ProcessingStage` |
| **Step** | Workflow step | `SetupStep`, `ExecutionStep` |
| **Action** | Executable action | `StartAction`, `StopAction` |
| **Plan** | Execution plan | `DeploymentPlan`, `ExecutionPlan` |
| **Pipeline** | Pipeline | `CI/CD Pipeline`, `DataPipeline` |

---

### 6. State & Lifecycle Management

| Term | Application Scenario | Example |
|------|----------------------|---------|
| **StateManager** | State management | `JobStateManager`, `TaskStateManager` |
| **LifecycleManager** | Lifecycle management | `ContainerLifecycleManager` |
| **StatusReporter** | State reporting | `NodeStatusReporter`, `PodStatusReporter` |
| **HealthChecker** | Health check | `ServiceHealthChecker`, `NodeHealthChecker` |
| **ReadinessProbe** | Readiness probe | `HTTPReadinessProbe`, `ScriptReadinessProbe` |
| **LivenessProbe** | Liveness probe | `TCPLivenessProbe` |
| **Starter** | Starter | `PodStarter`, `ServiceStarter` |
| **Terminator** | Terminator | `JobTerminator`, `PodTerminator` |

---

## 🧱 III. Naming Template and Structural Recommendations

| Type | Naming Template | Example |
|------|-----------------|---------|
| **Class Name** | `{Resource}{Action}{Role}` | `JobScheduler`, `NodeReconciler` |
| **Interface Name** | `I{Action}{Resource}` (C#) or `{Resource}{Action}` (Go) | `IScheduler`, `Scheduler`, `NodeSelector` |
| **Function Name** | `{Verb}{Resource}{Mode}` | `ScheduleJobNow`, `ReconcileNodeState` |
| **Variable Name** | `{Resource}{State}{Type}` | `jobStatus`, `lastScheduledTime` |

---

## ✅ IV. Naming Style Recommendations (By Language)

| Language | Recommended Style |
|---------|------------------|
| **Go** | CamelCase (lowercase initial), e.g., `nodeSelector`, `jobScheduler` |
| **Java** | CamelCase (lowercase initial), e.g., `nodeSelector`, `jobScheduler` |
| **C++** | CamelCase or underscore, e.g., `NodeSelector`, `job_scheduler` |
| **Python** | Underscore naming, e.g., `node_selector`, `job_scheduler` |
| **Kubernetes** | CamelCase recommended, e.g., `PodReconciler`, `StatefulSetController` |

---

## 📚 V. Naming Reference Examples (Kubernetes Style)

| Component | Naming |
|----------|--------|
| Controller | `ReplicaSetController`, `DeploymentController` |
| Scheduler | `DefaultScheduler`, `CustomScheduler` |
| Reconciler | `PodReconciler`, `ServiceReconciler` |
| Selector | `NodeSelector`, `AffinitySelector` |
| Probe | `LivenessProbe`, `ReadinessProbe` |
| Manager | `ResourceManager`, `VolumeManager` |
| Agent | `Kubelet`, `NodeAgent` |
| Executor | `ContainerExecutor`, `RemoteExecutor` |

---

## Synchronization
In software development, "synchronization" is a widely present concept involving concurrent control, data consistency, state synchronization, resource coordination, and more. To help you systematically name modules, classes, functions, or variables related to "synchronization", the following **synchronization domain naming recommendations** categorize terms by different scenarios and semantics.

---

### 🧩 I. Common Semantic Categories in Synchronization

| Type | Description | Example Scenario |
|------|-------------|------------------|
| **Concurrent Control** | Control execution order of multiple threads/coroutines/tasks | Mutex locks, semaphores, barriers |
| **Data Synchronization** | Ensure data consistency across replicas/systems/nodes | Database master-slave sync, cache sync |
| **State Synchronization** | Maintain state consistency | UI-model sync, service state sync |
| **Event Synchronization** | Control event trigger order/response logic | Synchronous event handling, waiting for event completion |
| **Resource Synchronization** | Coordinate access to shared resources | File sync, shared memory sync |
| **Time Synchronization** | Ensure time consistency across nodes | NTP, timestamp sync |
| **Task Synchronization** | Control task execution order/dependencies | Task queues, dependency scheduling |

---

### 📌 II. Synchronization-Related Terminology (By Category)

#### 1. Synchronization Control
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Sync** | General synchronization | `SyncData`, `SyncManager` |
| **Wait** | Wait for synchronization completion | `WaitForCompletion`, `WaitGroup` |
| **Lock** | Lock mechanism | `MutexLock`, `ReadLock` |
| **Semaphore** | Semaphore control | `ResourceSemaphore` |
| **Barrier** | Barrier synchronization | `TaskBarrier` |
| **Condition / Cond** | Condition variable | `ConditionVariable` |
| **Synchronizer** | Synchronization coordinator | `StateSynchronizer` |
| **Coordinator** | Coordinate multiple synchronization operations | `SyncCoordinator` |

---

#### 2. Data Synchronization
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Replicator** | Data replication | `DatabaseReplicator` |
| **Syncer** | Data synchronizer | `CacheSyncer`, `FileSyncer` |
| **Updater** | Data update | `StateUpdater`, `DataUpdater` |
| **Refresher** | Data refresh | `TokenRefresher`, `UIRefresher` |
| **Merger** | Data merging | `DeltaMerger`, `ConflictMerger` |
| **Resolver** | Conflict resolution | `ConflictResolver` |
| **Reconciler** | State reconciliation (Kubernetes style) | `ResourceReconciler` |
| **ConsistencyChecker** | Consistency verification | `DataConsistencyChecker` |

---

#### 3. State Synchronization
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **StateSynchronizer** | State synchronization | `UIStateSynchronizer` |
| **StateManager** | State management | `SessionStateManager` |
| **SyncState** | Synchronization state | `SyncState`, `ReplicaSyncState` |
| **Watcher** | State monitoring | `StateWatcher`, `VariableWatcher` |
| **Observer** | State observer | `ModelStateObserver` |
| **Notifier** | State change notification | `StateChangeNotifier` |
| **Tracker** | State tracking | `ProgressTracker`, `SyncProgressTracker` |

---

#### 4. Event Synchronization
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **EventHandler** | Event handling | `SyncEventHandler` |
| **Dispatcher** | Event dispatching | `SyncEventDispatcher` |
| **Listener** | Event monitoring | `SyncEventListener` |
| **Notifier** | Event notification | `SyncNotifier` |
| **Completer** | Event completion notification | `TaskCompleter` |
| **Trigger** | Trigger synchronization action | `SyncTrigger` |

---

#### 5. Time Synchronization
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Clock** | Time source | `SystemClock`, `SyncClock` |
| **TimeSynchronizer** | Time synchronization | `NTPSynchronizer` |
| **Timestamp** | Timestamp processing | `TimestampProvider` |
| **DriftDetector** | Clock drift detection | `ClockDriftDetector` |
| **SyncMonitor** | Time synchronization monitoring | `TimeSyncMonitor` |

---

#### 6. Task Synchronization
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **TaskScheduler** | Task scheduling | `SyncTaskScheduler` |
| **DependencyResolver** | Task dependencies | `TaskDependencyResolver` |
| **Worker** | Execute synchronous tasks | `SyncWorker` |
| **Queue** | Synchronous task queue | `SyncTaskQueue` |
| **Runner** | Executor | `SyncTaskRunner` |
| **Controller** | Control synchronization flow | `SyncTaskController` |

---

### 🧱 III. Naming Recommendation Examples

| Scenario | Example Naming |
|---------|----------------|
| **General Synchronization** | `SyncManager`, `Synchronizer`, `SyncController` |
| **Data Synchronization** | `DataSyncer`, `CacheSyncer`, `FileSyncer` |
| **State Synchronization** | `StateSynchronizer`, `UIStateSyncer` |
| **Concurrent Control** | `MutexLock`, `WaitGroup`, `Semaphore` |
| **Event Synchronization** | `SyncEventListener`, `SyncNotifier` |
| **Task Synchronization** | `SyncTaskQueue`, `SyncWorker`, `TaskSynchronizer` |
| **Time Synchronization** | `TimeSynchronizer`, `ClockDriftDetector` |

---

### ✅ IV. Best Naming Practice Recommendations

| Recommendation | Description |
|----------------|-------------|
| **Use Verb+Noun Structure** | E.g., `SyncData`, `WaitForCompletion` |
| **Consistent Prefix/Suffix Style** | E.g., consistently use suffixes like `Synchronizer`, `Syncer`, `Controller` |
| **Avoid Vague Terms** | E.g., `Manager`, `Handler` lack clear meaning when used alone - combine with context |
| **Use Domain Terminology** | E.g., use `Reconciler`, `Replicator` in distributed systems |
| **Differentiate Synchronous & Asynchronous** | E.g., `SyncWorker` vs `AsyncWorker`, `SyncTask` vs `BackgroundTask` |

---

### 📚 V. Naming Reference Templates

| Type | Template | Example |
|------|----------|---------|
| **Class Name** | `{Resource}{Action}{Role}` | `DataSyncer`, `StateSynchronizer` |
| **Function Name** | `{Verb}{Resource}{Mode}` | `SyncDataNow`, `WaitForSyncComplete` |
| **Variable Name** | `{Resource}{State}{Type}` | `syncInProgress`, `lastSyncTime` |
| **Interface Name** | `I{Action}{Resource}` (C#) or `{Resource}{Action}` (Go) | `ISyncHandler`, `Syncable` |

---

## 🛠 Utility Class Naming Supplement (Utility / Tooling)

In software systems, utility classes are typically used to encapsulate general functions, auxiliary operations, data processing, debugging support, etc. Below are commonly used English terms applicable to naming utility classes, auxiliary modules, or functions.

### 1. General Utility Class Naming
| Term | Application Scenario | Example |
|------|----------------------|---------|
| **Utils / Utilities** | General utility functions | `StringUtils`, `FileUtils` |
| **Helper** | Auxiliary class/function | `ConfigHelper`, `DBHelper` |
| **Tool / Toolkit** | Toolset or toolkit | `ImageTool`, `NetworkToolkit` |
| **Handler** | Event/request handling | `RequestHandler`, `EventHandler` |
| **Adapter** | Interface conversion/adapter | `LegacyDataAdapter`, `HTTPAdapter` |
| **Wrapper** | Encapsulate third-party interfaces/system calls | `CronWrapper`, `GRPCWrapper` |
| **Manager** | Resource management | `SessionManager`, `CacheManager` |
| **Provider** | Resource provider | `ConfigProvider`, `AuthProvider` |
| **Factory** | Object creation factory | `ConnectionFactory`, `LoggerFactory` |
| **Builder** | Builder pattern | `QueryBuilder`, `ApplicationBuilder` |
| **Registry** | Registration center | `PluginRegistry`, `TypeRegistry` |
| **Controller** | Control logic coordination | `JobController`, `FlowController` |
| **Dispatcher** | Event/task dispatching | `EventDispatcher`, `TaskDispatcher` |
| **Loader** | Data/resource loading | `ImageLoader`, `PluginLoader` |
| **Resolver** | Resolution logic | `DNSResolver`, `TypeResolver` |
| **Validator** | Data validation | `InputValidator`, `SchemaValidator` |
| **Converter** | Data format conversion | `JSONConverter`, `UnitConverter` |
| **Serializer / Deserializer** | Serialization/deserialization | `ProtobufSerializer` |
| **Monitor** | Monitoring tool | `SystemMonitor`, `HealthMonitor` |
| **Recorder** | Data recording | `MetricRecorder`, `EventRecorder` |

---

## 🖥 Observation, Diagnosis, Sniffing, Inspection, Review Domain

In software system runtime state observation, perspective, and review scenarios, the following English terms and metaphors can serve as naming references, organized by category:

---

### I. Core Conceptual Terms
| Term | Application Scenario | Description |
|------|----------------------|-------------|
| **Monitor** | Real-time monitoring | Most general term, e.g., `SystemMonitor` |
| **Observer** | Observer pattern | Used in event-driven systems (e.g., `EventObserver`) |
| **Watcher** | File/state change monitoring | E.g., `FileWatcher`, `ResourceWatcher` |
| **Inspector** | Deep inspection | Emphasizes diagnostic capability (browser dev tools `Inspector`) |
| **Profiler** | Performance analysis | Focuses on performance data collection (e.g., `CPUProfiler`) |
| **Sniffer** | Network/packet sniffing | E.g., `NetworkSniffer` |
| **Tracer** | Call chain tracing | Common in distributed systems (e.g., OpenTelemetry Tracer) |
| **Analyzer** | Data analysis | Focuses on post-processing (e.g., `LogAnalyzer`) |
| **Auditor** | Security/compliance review | Emphasizes audit functionality (e.g., `SecurityAuditor`) |
| **Check** | State/health check | `HealthCheck`, `LivenessCheck` |
| **Detect** | Automatic identification/detection | `LanguageDetector`, `AnomalyDetector` |
| **Trace** | Call chain tracking | `TraceCollector`, `TraceExporter` |
| **Log** | Log recording | `AccessLogger`, `AuditLogger` |
| **Capture** | Data capture | `PacketCapture`, `ScreenCapture` |
| **Dump** | Data export | `HeapDump`, `ThreadDump` |
| **Report** | Report generation | `ErrorReporter`, `UsageReporter` |
| **Scan** | Scanning inspection | `PortScanner`, `CodeScanner` |
| **Probe** | System state probing | `LivenessProbe`, `ReadinessProbe` |
| **Survey** | Comprehensive evaluation | `SystemSurvey`, `CodeSurvey` |
| **Inspect** | Deep examination | `ObjectInspector`, `RuntimeInspector` |
| **Profile** | Performance profiling | `MemoryProfiler`, `ExecutionProfiler` |
| **Audit** | Security/compliance review | `AccessAuditor`, `PolicyAuditor` |
| **Verify** | Verification | `SignatureVerifier`, `DataVerifier` |
| **Validate** | Data validation | `InputValidator`, `SchemaValidator` |

---

### II. Tool/Interface Terms