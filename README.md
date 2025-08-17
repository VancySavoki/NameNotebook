# 🔍 NameNotebook

<p align="right">
  <a href="README_EN.md">English</a> |
  <a href="README.md">中文版</a>
</p>

<div align="center">
  <h1>NameNotebook</h1>
  <h3>A notebook that explains how to name a project or variable effectively.</h3>
</div>


## 分布式调度、编排领域
在**分布式系统、编排系统、任务调度系统**等复杂系统设计中，命名不仅是代码可读性的关键，也是系统架构表达的重要组成部分。以下是一份**专业、系统化、可落地**的命名规范建议，涵盖**分布式协调、任务编排、资源调度、状态管理、节点通信、弹性伸缩**等核心领域。

---

## 🧩 一、命名原则（适用于分布式、编排、调度领域）

| 原则 | 说明 |
|------|------|
| **语义清晰** | 名称应准确表达其功能或职责，避免模糊词汇（如 `Manager`, `Handler` 单独使用时意义不明确）。 |
| **统一风格** | 同一模块或系统中使用一致的命名风格（如 `Controller`, `Coordinator`, `Scheduler` 等）。 |
| **结构化命名** | 推荐使用 `{资源}{操作}{角色}` 的结构化方式，如 `JobScheduler`, `NodeReconciler`。 |
| **领域术语优先** | 使用行业通用术语，如 `Orchestrator`, `Scheduler`, `Reconciler`, `Controller`, `Agent` 等。 |
| **区分同步与异步** | 如 `SyncWorker` vs `AsyncWorker`, `SyncTask` vs `BackgroundTask`。 |
| **区分状态与行为** | 如 `NodeState` vs `NodeStateManager`, `JobStatus` vs `JobScheduler`。 |

---

## 📌 二、核心组件命名建议（按功能分类）

### **1. 分布式协调（Distributed Coordination）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Coordinator** | 分布式协调器 | `TaskCoordinator`, `ClusterCoordinator` |
| **LeaderElector** | 领导选举机制 | `ETCDLeaderElector`, `RaftLeaderElector` |
| **LockManager** | 分布式锁管理 | `DistributedLockManager`, `ZooKeeperLockManager` |
| **MembershipManager** | 节点成员管理 | `ClusterMembershipManager` |
| **DiscoveryService** | 节点/服务发现 | `ServiceDiscovery`, `NodeDiscovery` |
| **Consensus** | 共识算法 | `RaftConsensus`, `PaxosConsensus` |
| **Barrier** | 分布式屏障同步 | `DistributedBarrier`, `TaskBarrier` |
| **Registry** | 资源注册中心 | `ServiceRegistry`, `NodeRegistry` |

---

### **2. 编排系统（Orchestration）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Orchestrator** | 核心编排器 | `DeploymentOrchestrator`, `WorkflowOrchestrator` |
| **Reconciler** | 状态调和器（Kubernetes 风格） | `PodReconciler`, `StatefulSetReconciler` |
| **Controller** | 控制器 | `ReplicaSetController`, `DeploymentController` |
| **Planner** | 执行计划制定 | `ExecutionPlanner`, `ResourcePlanner` |
| **Dispatcher** | 任务分发器 | `TaskDispatcher`, `ActionDispatcher` |
| **Executor** | 任务执行器 | `RemoteExecutor`, `ContainerExecutor` |
| **Agent** | 节点代理 | `NodeAgent`, `WorkerAgent` |
| **Worker** | 工作节点 | `TaskWorker`, `ExecutionWorker` |

---

### **3. 调度系统（Scheduling）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Scheduler** | 通用调度器 | `JobScheduler`, `TaskScheduler` |
| **Dispatcher** | 调度任务分发 | `ScheduleDispatcher` |
| **PreemptionManager** | 优先级抢占管理 | `JobPreemptionManager` |
| **QueueManager** | 调度队列管理 | `PriorityQueueManager` |
| **SchedulerPolicy** | 调度策略 | `RoundRobinPolicy`, `LeastUsedPolicy` |
| **NodeSelector** | 节点选择器 | `NodeSelector`, `AffinitySelector` |
| **ResourceAllocator** | 资源分配器 | `CPUAllocator`, `GPUAllocator` |
| **SchedulerExtender** | 调度器扩展 | `CustomSchedulerExtender` |

---

### **4. 资源管理（Resource Management）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **ResourceManager** | 资源管理 | `ClusterResourceManager`, `NodeResourceManager` |
| **ResourceMonitor** | 资源监控 | `MemoryMonitor`, `CPUUsageMonitor` |
| **CapacityManager** | 容量管理 | `NodeCapacityManager` |
| **QuotaManager** | 配额管理 | `TenantQuotaManager`, `ResourceQuotaManager` |
| **Allocator** | 资源分配 | `IPAllocator`, `PortAllocator` |
| **Provisioner** | 资源供给 | `VolumeProvisioner`, `NodeProvisioner` |
| **Scaler** | 弹性伸缩 | `AutoScaler`, `ReplicaScaler` |

---

### **5. 任务与工作流（Task & Workflow）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Job** | 任务单元 | `BatchJob`, `CronJob` |
| **Task** | 子任务 | `MapTask`, `ReduceTask` |
| **Workflow** | 工作流 | `DAGWorkflow`, `SequentialWorkflow` |
| **Stage** | 工作流阶段 | `ExecutionStage`, `ProcessingStage` |
| **Step** | 工作流步骤 | `SetupStep`, `ExecutionStep` |
| **Action** | 可执行操作 | `StartAction`, `StopAction` |
| **Plan** | 执行计划 | `DeploymentPlan`, `ExecutionPlan` |
| **Pipeline** | 流水线 | `CI/CD Pipeline`, `DataPipeline` |

---

### **6. 状态与生命周期管理（State & Lifecycle）**

| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **StateManager** | 状态管理 | `JobStateManager`, `TaskStateManager` |
| **LifecycleManager** | 生命周期管理 | `ContainerLifecycleManager` |
| **StatusReporter** | 状态上报 | `NodeStatusReporter`, `PodStatusReporter` |
| **HealthChecker** | 健康检查 | `ServiceHealthChecker`, `NodeHealthChecker` |
| **ReadinessProbe** | 就绪探针 | `HTTPReadinessProbe`, `ScriptReadinessProbe` |
| **LivenessProbe** | 存活探针 | `TCPLivenessProbe` |
| **Starter** | 启动器 | `PodStarter`, `ServiceStarter` |
| **Terminator** | 终止器 | `JobTerminator`, `PodTerminator` |

---

## 🧱 三、命名模板与结构建议

| 类型 | 命名模板 | 示例 |
|------|----------|------|
| **类名** | `{资源}{操作}{角色}` | `JobScheduler`, `NodeReconciler` |
| **接口名** | `I{操作}{资源}`（C#）或 `{Resource}{Operation}`（Go） | `IScheduler`, `Scheduler`, `NodeSelector` |
| **函数名** | `{动词}{资源}{方式}` | `ScheduleJobNow`, `ReconcileNodeState` |
| **变量名** | `{资源}{状态}{类型}` | `jobStatus`, `lastScheduledTime` |

---

## ✅ 四、命名风格推荐（按语言）

| 语言 | 推荐风格 |
|------|----------|
| **Go** | 驼峰命名（首字母小写），如 `nodeSelector`, `jobScheduler` |
| **Java** | 驼峰命名（首字母小写），如 `nodeSelector`, `jobScheduler` |
| **C++** | 驼峰命名或下划线命名，如 `NodeSelector`, `job_scheduler` |
| **Python** | 下划线命名，如 `node_selector`, `job_scheduler` |
| **Kubernetes** | 推荐使用 `CamelCase`，如 `PodReconciler`, `StatefulSetController` |

---

## 📚 五、命名参考案例（Kubernetes 风格）

| 组件 | 命名 |
|------|------|
| 控制器 | `ReplicaSetController`, `DeploymentController` |
| 调度器 | `DefaultScheduler`, `CustomScheduler` |
| 调和器 | `PodReconciler`, `ServiceReconciler` |
| 选择器 | `NodeSelector`, `AffinitySelector` |
| 探针 | `LivenessProbe`, `ReadinessProbe` |
| 管理器 | `ResourceManager`, `VolumeManager` |
| 代理 | `Kubelet`, `NodeAgent` |
| 执行器 | `ContainerExecutor`, `RemoteExecutor` |

---

## 同步
在软件开发中，“同步”是一个广泛存在的概念，涉及并发控制、数据一致性、状态同步、资源协调等多个方面。为了帮助你更系统地命名与“同步”相关的模块、类、函数或变量，以下是一份**同步领域命名建议指南**，按不同场景和语义进行分类。

---

### 🧩 一、同步领域常见语义分类

| 类型 | 描述 | 示例场景 |
|------|------|----------|
| **并发控制** | 控制多个线程/协程/任务的执行顺序 | 互斥锁、信号量、屏障 |
| **数据同步** | 保证多个副本、系统、节点之间的数据一致性 | 数据库主从同步、缓存同步 |
| **状态同步** | 保持状态的一致性 | UI 与模型同步、服务状态同步 |
| **事件同步** | 控制事件的触发顺序或响应逻辑 | 同步事件处理、等待事件完成 |
| **资源同步** | 协调多个组件对共享资源的访问 | 文件同步、共享内存同步 |
| **时间同步** | 保证多个节点的时间一致 | NTP、时间戳同步 |
| **任务同步** | 控制任务的执行顺序或依赖关系 | 任务队列、依赖调度 |

---

### 📌 二、同步相关命名词汇（按类别整理）

#### **1. 同步控制类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Sync** | 通用同步操作 | `SyncData`, `SyncManager` |
| **Wait** | 等待同步完成 | `WaitForCompletion`, `WaitGroup` |
| **Lock** | 锁机制 | `MutexLock`, `ReadLock` |
| **Semaphore** | 信号量控制 | `ResourceSemaphore` |
| **Barrier** | 屏障同步 | `TaskBarrier` |
| **Condition / Cond** | 条件变量 | `ConditionVariable` |
| **Synchronizer** | 同步协调器 | `StateSynchronizer` |
| **Coordinator** | 协调多个同步操作 | `SyncCoordinator` |

---

#### **2. 数据同步类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Replicator** | 数据复制 | `DatabaseReplicator` |
| **Syncer** | 数据同步器 | `CacheSyncer`, `FileSyncer` |
| **Updater** | 数据更新 | `StateUpdater`, `DataUpdater` |
| **Refresher** | 数据刷新 | `TokenRefresher`, `UIRefresher` |
| **Merger** | 数据合并 | `DeltaMerger`, `ConflictMerger` |
| **Resolver** | 冲突解决 | `ConflictResolver` |
| **Reconciler** | 状态调和（Kubernetes 风格） | `ResourceReconciler` |
| **ConsistencyChecker** | 一致性校验 | `DataConsistencyChecker` |

---

#### **3. 状态同步类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **StateSynchronizer** | 状态同步 | `UIStateSynchronizer` |
| **StateManager** | 状态管理 | `SessionStateManager` |
| **SyncState** | 同步状态 | `SyncState`, `ReplicaSyncState` |
| **Watcher** | 状态监听 | `StateWatcher`, `VariableWatcher` |
| **Observer** | 状态观察者 | `ModelStateObserver` |
| **Notifier** | 状态变更通知 | `StateChangeNotifier` |
| **Tracker** | 状态追踪 | `ProgressTracker`, `SyncProgressTracker` |

---

#### **4. 事件同步类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **EventHandler** | 事件处理 | `SyncEventHandler` |
| **Dispatcher** | 事件分发 | `SyncEventDispatcher` |
| **Listener** | 事件监听 | `SyncEventListener` |
| **Notifier** | 事件通知 | `SyncNotifier` |
| **Completer** | 事件完成通知 | `TaskCompleter` |
| **Trigger** | 触发同步动作 | `SyncTrigger` |

---

#### **5. 时间同步类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Clock** | 时间源 | `SystemClock`, `SyncClock` |
| **TimeSynchronizer** | 时间同步 | `NTPSynchronizer` |
| **Timestamp** | 时间戳处理 | `TimestampProvider` |
| **DriftDetector** | 时钟漂移检测 | `ClockDriftDetector` |
| **SyncMonitor** | 时间同步监控 | `TimeSyncMonitor` |

---

#### **6. 任务同步类**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **TaskScheduler** | 任务调度 | `SyncTaskScheduler` |
| **DependencyResolver** | 任务依赖 | `TaskDependencyResolver` |
| **Worker** | 执行同步任务 | `SyncWorker` |
| **Queue** | 同步任务队列 | `SyncTaskQueue` |
| **Runner** | 执行器 | `SyncTaskRunner` |
| **Controller** | 控制同步流程 | `SyncTaskController` |

---

### 🧱 三、命名建议组合示例

| 场景 | 示例命名 |
|------|----------|
| **通用同步** | `SyncManager`, `Synchronizer`, `SyncController` |
| **数据同步** | `DataSyncer`, `CacheSyncer`, `FileSyncer` |
| **状态同步** | `StateSynchronizer`, `UIStateSyncer` |
| **并发控制** | `MutexLock`, `WaitGroup`, `Semaphore` |
| **事件同步** | `SyncEventListener`, `SyncNotifier` |
| **任务同步** | `SyncTaskQueue`, `SyncWorker`, `TaskSynchronizer` |
| **时间同步** | `TimeSynchronizer`, `ClockDriftDetector` |

---

### ✅ 四、命名最佳实践建议

| 建议 | 说明 |
|------|------|
| **使用动词+名词结构** | 如 `SyncData`, `WaitForCompletion` |
| **统一前缀/后缀风格** | 如统一使用 `Synchronizer`、`Syncer`、`Controller` 等后缀 |
| **避免模糊词汇** | 如 `Manager`, `Handler` 单独使用时意义不明确，建议结合上下文 |
| **结合领域术语** | 如在分布式系统中使用 `Reconciler`、`Replicator` 等术语 |
| **区分同步与异步** | 如 `SyncWorker` vs `AsyncWorker`，`SyncTask` vs `BackgroundTask` |

---

### 📚 五、命名参考模板

| 类型 | 模板 | 示例 |
|------|------|------|
| **类名** | `{资源}{操作}{角色}` | `DataSyncer`, `StateSynchronizer` |
| **函数名** | `{动词}{资源}{方式}` | `SyncDataNow`, `WaitForSyncComplete` |
| **变量名** | `{资源}{状态}{类型}` | `syncInProgress`, `lastSyncTime` |
| **接口名** | `I{操作}{资源}`（C#）或 `{Resource}{Operation}`（Go） | `ISyncHandler`, `Syncable` |

---


## 🛠 工具类命名补充（Utility / Tooling）

在软件系统中，工具类通常用于封装通用功能、辅助操作、数据处理、调试支持等。以下是一些常用的英文词汇，适用于命名工具类、辅助模块或函数。

### **1. 通用工具类命名**
| 单词 | 适用场景 | 示例 |
|------|----------|------|
| **Utils / Utilities** | 通用工具函数集合 | `StringUtils`, `FileUtils` |
| **Helper** | 辅助类或函数 | `ConfigHelper`, `DBHelper` |
| **Tool / Toolkit** | 工具集或工具包 | `ImageTool`, `NetworkToolkit` |
| **Handler** | 事件或请求处理 | `RequestHandler`, `EventHandler` |
| **Adapter** | 接口转换或适配 | `LegacyDataAdapter`, `HTTPAdapter` |
| **Wrapper** | 封装第三方接口或系统调用 | `CronWrapper`, `GRPCWrapper` |
| **Manager** | 资源管理 | `SessionManager`, `CacheManager` |
| **Provider** | 资源提供者 | `ConfigProvider`, `AuthProvider` |
| **Factory** | 对象创建工厂 | `ConnectionFactory`, `LoggerFactory` |
| **Builder** | 构造器模式 | `QueryBuilder`, `ApplicationBuilder` |
| **Registry** | 注册中心 | `PluginRegistry`, `TypeRegistry` |
| **Controller** | 控制逻辑协调 | `JobController`, `FlowController` |
| **Dispatcher** | 事件或任务分发 | `EventDispatcher`, `TaskDispatcher` |
| **Loader** | 数据或资源加载 | `ImageLoader`, `PluginLoader` |
| **Resolver** | 解析逻辑 | `DNSResolver`, `TypeResolver` |
| **Validator** | 数据校验 | `InputValidator`, `SchemaValidator` |
| **Converter** | 数据格式转换 | `JSONConverter`, `UnitConverter` |
| **Serializer / Deserializer** | 序列化与反序列化 | `ProtobufSerializer` |
| **Monitor** | 监控工具 | `SystemMonitor`, `HealthMonitor` |
| **Recorder** | 数据记录 | `MetricRecorder`, `EventRecorder` |


## 🖥 观测、诊断、嗅探、检查、审查领域

在软件系统运行时状态的观测、透视、审查等场景中，以下英文词汇和隐喻可以作为命名参考，按类别整理：

---

### **一、核心概念类**
| 单词 | 适用场景 | 说明 |
|------|----------|------|
| **Monitor** | 实时监控 | 最通用术语，如 `SystemMonitor` |
| **Observer** | 观察者模式 | 用于事件驱动系统（如 `EventObserver`） |
| **Watcher** | 文件/状态变化监控 | 如 `FileWatcher`、`ResourceWatcher` |
| **Inspector** | 深度检查 | 强调诊断能力（如浏览器开发者工具的 `Inspector`） |
| **Profiler** | 性能分析 | 侧重性能数据采集（如 `CPUProfiler`） |
| **Sniffer** | 网络/数据包嗅探 | 如 `NetworkSniffer` |
| **Tracer** | 调用链追踪 | 分布式系统中常见（如 `OpenTelemetry Tracer`） |
| **Analyzer** | 数据分析 | 侧重后处理（如 `LogAnalyzer`） |
| **Auditor** | 安全/合规审查 | 强调审计功能（如 `SecurityAuditor`） |
| **Check** | 状态/健康检查 | `HealthCheck`, `LivenessCheck` |
| **Detect** | 自动识别/检测 | `LanguageDetector`, `AnomalyDetector` |
| **Trace** | 调用链跟踪 | `TraceCollector`, `TraceExporter` |
| **Log** | 日志记录 | `AccessLogger`, `AuditLogger` |
| **Capture** | 数据捕获 | `PacketCapture`, `ScreenCapture` |
| **Dump** | 数据导出 | `HeapDump`, `ThreadDump` |
| **Report** | 报告生成 | `ErrorReporter`, `UsageReporter` |
| **Scan** | 扫描检查 | `PortScanner`, `CodeScanner` |
| **Probe** | 探测系统状态 | `LivenessProbe`, `ReadinessProbe` |
| **Survey** | 综合性评估 | `SystemSurvey`, `CodeSurvey` |
| **Inspect** | 深度查看 | `ObjectInspector`, `RuntimeInspector` |
| **Profile** | 性能画像 | `MemoryProfiler`, `ExecutionProfiler` |
| **Audit** | 安全/合规审查 | `AccessAuditor`, `PolicyAuditor` |
| **Verify** | 校验验证 | `SignatureVerifier`, `DataVerifier` |
| **Validate** | 数据验证 | `InputValidator`, `SchemaValidator` |

---

### **二、工具/界面类**
| 单词 | 适用场景 | 说明 |
|------|----------|------|
| **Dashboard** | 驾驶舱 | 最常用的可视化聚合界面（如 `Prometheus Dashboard`） |
| **Console** | 控制台 | 命令行或集成工具（如 `Kubernetes Dashboard`） |
| **Lens** | 数据透视 | 强调“透过现象看本质”（如 `DataLens`） |
| **Radar** | 实时态势感知 | 用于全局监控（如 `InfrastructureRadar`） |
| **Scope** | 范围分析 | 可表示观测范围（如 `NetworkScope`） |
| **Hub** | 数据中心 | 表示集中式观测节点（如 `ObservabilityHub`） |
| **Vault** | 安全观测 | 强调加密/敏感数据监控（如 `SecretVaultMonitor`） |
| **Portal** | 入口 | 作为观测系统的统一入口（如 `SystemPortal`） |
| **Dashboard** | 可视化展示 | `MonitoringDashboard`, `MetricsDashboard` |
| **Viewer** | 数据展示 | `LogViewer`, `TraceViewer` |
| **Explorer** | 数据浏览 | `APIExplorer`, `ObjectExplorer` |
| **Console** | 控制台 | `DeveloperConsole`, `DebugConsole` |
| **Reporter** | 报告生成 | `TestReporter`, `AlertReporter` |
| **Notifier** | 通知机制 | `EmailNotifier`, `SlackNotifier` |
| **Exporter** | 数据导出 | `PrometheusExporter`, `JSONExporter` |
| **Collector** | 数据采集 | `MetricCollector`, `TraceCollector` |
| **Aggregator** | 数据聚合 | `LogAggregator`, `MetricAggregator` |
| **Presenter** | 数据格式化展示 | `ResultPresenter`, `UIPresenter` |

---

### **三、隐喻类（抽象表达）**
| 单词 | 适用场景 | 说明 |
|------|----------|------|
| **Telescope** | 远程观测 | 强调远距离或宏观视角（如 `ClusterTelescope`） |
| **Microscope** | 微观分析 | 表示深度细粒度分析（如 `CodeMicroscope`） |
| **Mirror** | 实时镜像 | 表示系统状态的实时映射（如 `SystemMirror`） |
| **X-Ray** | 透析诊断 | 强调穿透式分析（如 `ServiceXRay`） |
| **Pulse** | 健康状态 | 表示心跳/健康检查（如 `SystemPulse`） |
| **Net** | 网络拓扑 | 用于网络连接监控（如 `ServiceNet`） |
| **Orbit** | 轨道监测 | 表示周期性或全局覆盖（如 `SatelliteOrbitMonitor`） |
| **Grid** | 网格化观测 | 用于分布式网格系统（如 `ServiceGrid`） |

---

### **四、数据流相关**
| 单词 | 适用场景 | 说明 |
|------|----------|------|
| **Stream** | 实时数据流 | 如 `LogStream`、`MetricsStream` |
| **Pipeline** | 数据处理链 | 表示观测数据的处理流程（如 `ObservabilityPipeline`） |
| **Buffer** | 数据缓存 | 表示临时存储观测数据（如 `TraceBuffer`） |
| **Channel** | 数据通道 | 用于模块间通信监控（如 `EventChannel`） |
| **Bridge** | 数据中继 | 表示不同系统间的观测数据桥接（如 `MetricsBridge`） |

---

### **五、组合命名示例**
| 词汇组合 | 适用场景 | 说明 |
|----------|----------|------|
| **LiveView** | 实时视图 | 如 `LiveSystemView` |
| **InsightEngine** | 洞察能力 | 强调分析深度（如 `PerformanceInsightEngine`） |
| **WatchTower** | 全局监控 | 隐喻“瞭望塔”（如 `CloudWatchTower`） |
| **SignalHub** | 信号中心 | 表示观测信号的聚合（如 `MetricSignalHub`） |
| **TraceScope** | 追踪范围 | 结合追踪与范围分析（如 `DistributedTraceScope`） |
