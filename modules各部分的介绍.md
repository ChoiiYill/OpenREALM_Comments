# realm_core
**子模块所在路径：/OpenREALM/modules/realm_core** <br>
该模块提供了一系列核心功能和类，用于处理图像、点云、深度图、相机模型、坐标转换、线程管理等操作。该模块依赖于多个第三方库，如 OpenCV、Eigen 和 GDAL，以实现高效的数据处理和计算。<br>
功能：为其他模块提供一些通用的数据结构和工具函数。<br>
链接库：主要使用了C++标准库，OpenCV和GDAL等第三方库<br>
主要有以下几个类：
- ### *CLASS – WorkerThreadBase*
  - 所属命名空间：realm
  - 对应的代码文件：worker_thread_base.h, worker_thread_base.cpp
  - 说明：WorkerThreadBase 类提供了一个基础的工作线程管理器，支持线程的启动、停止、重置和通知操作。它还包含统计处理时间的功能。
- ### *CLASS – Timer*
  - 所属命名空间：realm
  - 对应的代码文件：timer.h, timer.cpp
  - 说明：Timer 类提供了一个定时器功能，支持定时执行指定的函数，并提供获取当前时间的多种格式（秒、毫秒、微秒、纳秒）。
- ### *CLASS – Stereo*
  - 所属命名空间：realm::stereo
  - 对应的代码文件：stereo.h, stereo.cpp
  - 说明：Stereo 类提供了一些函数，用于计算立体校正、重映射图像、从深度图重投影点云、从点云计算深度图和法线图等操作。
- ### *CLASS – SettingsBase*
  - 所属命名空间：realm
  - 对应的代码文件：settings_base.h, settings_base.cpp
  - 说明：SettingsBase 类提供了一个通用的设置管理器，支持从文件加载设置、设置和获取参数值、打印设置等操作。它还支持参数的多种类型（整数、浮点数、字符串、矩阵）。
- ### *CLASS – PointCloud*
  - 所属命名空间：realm
  - 对应的代码文件：point_cloud.h, point_cloud.cpp
  - 说明：PointCloud 类提供了一个点云数据的容器，支持点云数据的存储、访问和基本操作。
- ### *CLASS – PlaneFitter*
  - 所属命名空间：realm
  - 对应的代码文件：plane_fitter.h, plane_fitter.cpp
  - 说明：PlaneFitter 类提供了一个平面拟合器，支持通过最小二乘法或精确解计算平面参数。
- ### *CLASS – Frame*
  - 所属命名空间：realm
  - 对应的代码文件：frame.h, frame.cpp
  - 说明：Frame 类是一个数据容器，用于存储和传递在管道中测量或计算的所有信息。它包含图像、深度图、点云、相机模型、姿态等数据。
- ### *CLASS – Depthmap*
  - 所属命名空间：realm
  - 对应的代码文件：depthmap.h, depthmap.cpp
  - 说明：Depthmap 类提供了一个深度图数据的容器，支持深度图数据的存储、访问和基本操作。它还包含计算最小、最大和中值深度的功能。
- ### *CLASS – CvGridMap*
  - 所属命名空间：realm
  - 对应的代码文件：cv_grid_map.h, cv_grid_map.cpp
  - 说明：CvGridMap 类提供了一个网格地图的容器，支持网格地图数据的存储、访问和基本操作。它还包含几何设置、分辨率调整、子地图提取等功能。
- ### *CLASS – Conversions*
  - 所属命名空间：realm::gis
  - 对应的代码文件：conversions.h, conversions.cpp
  - 说明：Conversions 类提供了一些函数，用于在 WGS84 和 UTM 坐标系之间进行转换。
- ### *CLASS – Camera*
  - 所属命名空间：realm::camera
  - 对应的代码文件：camera.h, camera.cpp
  - 说明：Camera 类提供了一个基础的针孔相机模型，支持相机参数的设置和获取、图像的去畸变、图像边界的计算等操作。
- ### *CLASS – CameraSettings*
  - 所属命名空间：realm
  - 对应的代码文件：camera_settings.h, camera_settings.cpp
  - 说明：CameraSettings 类提供了一个相机设置管理器，支持从文件加载相机设置、设置和获取相机参数等操作。
- ### *CLASS – CameraSettingsFactory*
  - 所属命名空间：realm
  - 对应的代码文件：camera_settings_factory.h, camera_settings_factory.cpp
  - 说明：CameraSettingsFactory 类提供了一个工厂类，用于从文件加载相机设置。
- ### *CLASS – Analysis*
  - 所属命名空间：realm::analysis
  - 对应的代码文件：analysis.h, analysis.cpp
  - 说明：Analysis 类提供了一些函数，用于将单通道或三通道的浮点矩阵转换为 RGB 颜色图。
- ### *CLASS – WGSPose*
  - 所属命名空间：realm
  - 对应的代码文件：wgs84.h
  - 说明：WGSPose 类用于表示 WGS84 坐标系下的位姿（位置和航向）。
- ### *CLASS – UTMPose*
  - 所属命名空间：realm
  - 对应的代码文件：utm32.h
  - 说明：UTMPose 类用于表示 UTM 坐标系下的位姿（位置和航向）。
- ### *CLASS – TreeNode*
  - 所属命名空间：realm
  - 对应的代码文件：tree_node.h
  - 说明：TreeNode 类提供了一个通用的树节点实现，支持树节点的添加、删除、查找和遍历等操作。
- ### *CLASS – ImuSettings*
  - 所属命名空间：realm
  - 对应的代码文件：imu_settings.h
  - 说明：ImuSettings 类提供了一个 IMU 设置管理器，支持从文件加载 IMU 设置、设置和获取 IMU 参数等操作。
- ### *CLASS – Structs*
  - 所属命名空间：realm
  - 对应的代码文件：structs.h
  - 说明：Structs 文件定义了一些基本的数据结构，如平面、参数和网格面等。

---
<br>

# realm_io
**子模块所在路径：/OpenREALM/modules/realm_io** <br>
提供了一整套工具，用于处理和管理各种输入输出操作。通过结合 OpenCV、Boost、GDAL 和 Exiv2 等库，它能够高效地进行文件和目录管理、图像和深度图的加载与保存、相机参数的加载与保存、地理空间数据的处理、点云数据的处理等操作<br>
功能：为其他模块提供一些通用的数据结构和工具函数。<br>
链接库：OpenCV、Boost、GDAL、Exiv2等<br>
主要有以下几个类：
- ### *CLASS – Utilities*
  - 所属命名空间：realm::io
  - 对应的代码文件：utilities.h, utilities.cpp
  - 说明：Utilities 类提供了一些实用函数，用于文件和目录的检查、创建和删除，以及生成唯一文件名、获取系统临时目录、获取当前日期时间、分割字符串等操作。
- ### *CLASS – RealmImport*
  - 所属命名空间：realm::io
  - 对应的代码文件：realm_import.h, realm_import.cpp
  - 说明：RealmImport 类提供了一些函数，用于从 YAML 文件加载相机参数和地理参考矩阵，从 TUM 格式的文本文件加载轨迹数据，从文本文件加载表面点云数据，以及从二进制文件加载 CvGridMap 数据。
- ### *CLASS – RealmExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：realm_export.h, realm_export.cpp
  - 说明：RealmExport 类提供了一些函数，用于保存时间戳、轨迹数据和 CvGridMap 数据到文件中。
- ### *CLASS – PclExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：pcl_export.h, pcl_export.cpp
  - 说明：PclExport 类提供了一些函数，用于将 CvGridMap 中的高程点云数据保存为 PLY 文件。
- ### *CLASS – MvsExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：mvs_export.h, mvs_export.cpp
  - 说明：MvsExport 类提供了一些函数，用于将帧数据保存为 MVS 格式的文件。
- ### *CLASS – GisExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：gis_export.h, gis_export.cpp
  - 说明：GisExport 类提供了一些函数，用于将 CvGridMap 数据保存为 GeoTIFF 文件，并提供了一些辅助函数用于生成 GDAL 数据集元数据和处理 GDAL 数据集。
- ### *CLASS – GdalContinuousWriter*
  - 所属命名空间：realm::io
  - 对应的代码文件：gdal_continuous_writer.h, gdal_continuous_writer.cpp
  - 说明：GdalContinuousWriter 类继承自 WorkerThreadBase，用于在后台线程中连续保存 GeoTIFF 文件。
- ### *CLASS – ExifImport*
  - 所属命名空间：realm::io
  - 对应的代码文件：exif_import.h, exif_import.cpp
  - 说明：ExifImport 类提供了一些函数，用于从图像文件中读取 Exif 元数据，并将其转换为帧数据。
- ### *CLASS – ExifExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：exif_export.h, exif_export.cpp
  - 说明：ExifExport 类提供了一些函数，用于将帧数据保存为带有 Exif 元数据的图像文件。
- ### *CLASS – CvImport*
  - 所属命名空间：realm::io
  - 对应的代码文件：cv_import.h, cv_import.cpp
  - 说明：CvImport 类提供了一些函数，用于从文件中加载图像数据，包括从二进制文件加载图像数据。
- ### *CLASS – CvExport*
  - 所属命名空间：realm::io
  - 对应的代码文件：cv_export.h, cv_export.cpp
  - 说明：CvExport 类提供了一些函数，用于将图像数据保存为文件，包括保存立体图像对、深度图和带有颜色映射的图像。

---
<br>

# realm_densifier
realm_densifier模块提供了一些点云加密功能，在稠密重建部分，通过使用优化后的相机姿态生成虚拟的立体对，并应用高效的立体匹配算法来计算稠密点云。<br>
## realm_densifier_base
**所在路径：/OpenREALM/modules/realm_densifier_base** <br>
功能：用的基本方法，为后续步骤生成稠密点云。<br>
链接库：主要使用了OpenCV，如果有使用CUDA的话也可以进行编译。<br>
主要有以下几个类：
- ### *CLASS - DensifierIF*
  - 所属命名空间：realm
  - 对应的代码文件：densifier_IF.h
  - 说明：接口类，主要功能是定义一个图像密集化的接口DensifierIF。它提供了用于处理多帧图像生成深度图的框架。该接口包括获取输入帧数量、缩放因子以及打印设置的功能，使得任何实现该接口的类都必须提供具体的实现。
- ### *CLASS – Dummy*
  - 所属命名空间：realm::densifier
  - 继承自：DensifierIF
  - 对应的代码文件：densifier_dummy.h、densifier_dummy.cpp
  - 说明：实现了一个Dummy类，作为DensifierIF接口的占位符实现。其主要功能是提供一个无操作的框架，可以在没有实际实现的情况下轻松集成到更大的系统中。此类通常用于测试、占位或将来扩展时提供简单的接口结构。
- ### *CLASS – DensifierFactory*
  - 所属命名空间：realm::densifier
  - 对应的代码文件：densifier_factory.h、densifier_factory.cpp
  - 说明：主要功能是提供一个工厂机制，通过动态加载不同的密集化框架来支持多种密集化算法。用户只需按照说明实现相应的接口和设置类，并提供相应的 YAML 配置文件，DensifierFactory 类就能够根据用户的需求创建对应的密集化处理实例。这种设计不仅提高了代码的灵活性和扩展性，还促进了不同框架的模块化集成。
- ### *CLASS – PlaneSweep*
  - 所属命名空间：realm::densifier
  - 继承自：[DensifierIF](#class---densifierif)
  - 对应的代码文件：plane_sweep.h、plane_sweep.cpp
  - 说明：通过平面扫掠算法从多帧图像中生成稠密深度图。其功能包括设置各种参数、处理多帧输入、计算和返回指定参考帧的深度图。
- ### *CLASS – DensifierSettings*
  - 所属命名空间：realm
  - 继承自：SettingsBase
  - 对应的代码文件：densifier_settings.h、densifier_settings.cpp
  - 说明：定义一个用于密集化过程设置的类。它提供了基本的参数配置，包括框架类型和图像缩放因子，同时支持将这些设置以 YAML 文件格式进行加载。
- ### *CLASS – DensifierDummySettings*
  - 所属命名空间：realm
  - 继承自：[DensifierSettings](#class--densifiersettings)
  - 对应的代码文件：densifier_settings.h、densifier_settings.cpp
  - 说明：构造函数没有定义任何属性或逻辑，这个类可能是在某种情况下需要快速创建一个空的设置实现，或者是为进一步扩展和实现做准备。
- ### *CLASS – PlaneSweepSettings*
  - 所属命名空间：realm
  - 继承自：[DensifierSettings](#class--densifiersettings)
  - 对应的代码文件：densifier_settings.h、densifier_settings.cpp
  - 说明：专门用于配置平面扫描算法的各种参数。通过这些参数，用户可以灵活地调整算法的行为，以满足不同场景重建的需求。
- ### *CLASS – DensifierSettingsFactory*
  - 所属命名空间：realm
  - 对应的代码文件：densifier_settings_factory.h、densifier_settings_factory.cpp
  - 说明：该代码文件提供了一个工厂类用于加载和管理密集化设置，支持通过 YAML 文件配置不同类型的设置，并包含了相应的模板方法以适应不同的配置需求。

## realm_densifier_impl
**所在路径：/OpenREALM/modules/realm_densifier_impl/psl** <br>
功能：用PSL库的方法，为后续步骤生成稠密点云。<br>
链接库：主要使用了OpenCV、PSL，如果有使用CUDA的话也可以进行编译。<br>
主要有以下几个类：
- ### *CLASS – ioTools*
  - 所属命名空间：PSL
  - 对应的代码文件：ioTools.h、ioTools.cpp
  - 说明：ioTools 类提供了一些用于文件路径处理和 OBJ 文件读取的实用函数。
- ### *CLASS – Grid*
  - 所属命名空间：PSL
  - 对应的代码文件：grid.h、grid.cpp
  - 说明：Grid 类是一个模板类，用于存储和管理三维网格数据。它提供了访问、克隆、调整大小、保存和加载网格数据的方法。
- ### *CLASS – FishEyeDepthMap*
  - 所属命名空间：PSL
  - 对应的代码文件：fishEyeDepthMap.h、fishEyeDepthMap.cpp
  - 说明：FishEyeDepthMap 类是一个模板类，用于存储和管理鱼眼相机的深度图数据。它提供了访问、显示、保存和导出深度图数据的方法。
- ### *CLASS – FishEyeCameraMatrix*
  - 所属命名空间：PSL
  - 对应的代码文件：fishEyeCameraMatrix.h、fishEyeCameraMatrix.cpp
  - 说明：FishEyeCameraMatrix 类是一个模板类，用于存储和管理鱼眼相机的相机矩阵。它提供了相机矩阵的设置、缩放、投影和反投影等功能。
- ### *CLASS – Exception*
  - 所属命名空间：PSL
  - 对应的代码文件：exception.h
  - 说明：Exception 类用于处理异常情况。它继承自标准库的 std::exception 类，并提供了自定义的异常消息格式。
- ### *CLASS – DeviceImage*
  - 所属命名空间：PSL
  - 对应的代码文件：deviceImage.h、deviceImage.cu、deviceImage.cpp
  - 说明：DeviceImage 类用于在 CUDA 设备上存储和管理图像数据。它提供了图像数据的分配、上传、下载和访问等功能。
- ### *CLASS – DeviceBuffer*
  - 所属命名空间：PSL
  - 对应的代码文件：deviceBuffer.h、deviceBuffer.cu、deviceBuffer.cpp
  - 说明：DeviceBuffer类是一个模板类，用于在CUDA设备上存储和管理缓冲区数据。它提供了缓冲区数据的分配、上传、下载和访问等功能。
- ### *CLASS – DepthMap*
  - 所属命名空间：PSL
  - 对应的代码文件：depthMap.h、depthMap.cpp
  - 说明：DepthMap类是一个模板类，用于存储和管理深度图数据。它提供了访问、显示、保存和导出深度图数据的方法。
- ### *CLASS – CudaPlaneSweep*
  - 所属命名空间：PSL
  - 对应的代码文件：cudaPlaneSweep.h、cudaPlaneSweep.cu、cudaPlaneSweep.cpp
  - 说明：CudaPlaneSweep 类用于在 CUDA 设备上执行平面扫描算法。它提供了添加图像、设置参数、处理图像和获取结果的方法。
- ### *CLASS – CudaFishEyePlaneSweep*
  - 所属命名空间：PSL
  - 对应的代码文件：cudaFishEyePlaneSweep.h、cudaFishEyePlaneSweep.cu、cudaFishEyePlaneSweep.cpp
  - 说明：CudaFishEyePlaneSweep 类用于在 CUDA 设备上执行鱼眼相机的平面扫描算法。它提供了添加图像、设置参数、处理图像和获取结果的方法。
- ### *CLASS – CudaFishEyeImageProcessor*
  - 所属命名空间：PSL
  - 对应的代码文件：cudaFishEyeImageProcessor.h、cudaFishEyeImageProcessor.cu、cudaFishEyeImageProcessor.cpp
  - 说明：CudaFishEyeImageProcessor 类用于在 CUDA 设备上处理鱼眼相机的图像。它提供了图像去畸变和提取针孔图像的方法。
- ### *CLASS – ConfigFile*
  - 所属命名空间：PSL
  - 对应的代码文件：configFile.h、configFile.cpp
  - 说明：ConfigFile 类用于读取和解析配置文件。它提供了获取配置参数的方法。
- ### *CLASS – Common*
  - 所属命名空间：PSL
  - 对应的代码文件：common.h
  - 说明：Common 文件包含一些通用的实用函数和宏定义，用于处理 CUDA 错误和计算瓦片数量。
- ### *CLASS – ColorMapJet*
  - 所属命名空间：PSL
  - 对应的代码文件：colorMapJet.h、colorMapJet.cpp
  - 说明：ColorMapJet 文件定义了一个颜色映射数组，用于将深度值映射到颜色值。
- ### *CLASS – CameraMatrix*
  - 所属命名空间：PSL
  - 对应的代码文件：cameraMatrix.h、cameraMatrix.cpp
  - 说明：CameraMatrix 类是一个模板类，用于存储和管理相机的投影矩阵。它提供了相机矩阵的设置、缩放、投影和反投影等功能。



---
<br>

# realm_vslam/realm_vslam_base
**所在路径：/OpenREALM/modules/realm_vslam/realm_vslam_base** <br>
功能：这个模块是提供了一个视觉SLAM的抽象基类，以及对OpenVSLAM和ORB_SLAM2的封装。它的功能是为其他模块提供一些视觉SLAM的接口和功能。它主要使用了OpenVSLAM和ORB_SLAM2等第三方库来实现。
1. 首先抓取图像和GNSS数据，并将其打包为“帧”
2. 尝试初始化单目SLAM
3. 一旦视觉SLAM初始化成功，尝试计算局部SLAM坐标系与全局地理坐标系（定义为东-北-上ENU）之间的变换，
<br>具体如下：
- 根据当前的GNSS位置与前一个测量的视觉位置的比值计算平均比例
- 计算平均参考平面的法向量
- 缓冲区内的测量次数超过3次？是 -> 继续 / 否 -> 返回
- 比例是否收敛到限制值以下？参考平面的法向量是否收敛到限制值以下？
- 如果都满足，则初始化参考平面坐标系
- 将参考平面中视觉姿态的2D相似性变换计算为GNSS（utm32）东/北（不考虑高度）
- 计算从局部坐标系到ENU的总变换
4. 将地理参考应用于帧的姿态和地图点
5. 发布帧<br>

链接库：主要使用了realm_core、realm_io、OpenCV、OpenVSLAM、ORB_SLAM2、Eigen3。<br>
主要有以下几个类：
- ### *CLASS – VisualSlamIF*
  - 所属命名空间：realm
  - 对应的代码文件：visual_slam_IF.h
  - 说明：定义了一个视觉SLAM接口类VisualSlamIF，其主要目的在于提供一个标准化接口，供不同的视觉SLAM实现使用。它定义了一系列必要的函数和数据结构，包括用于处理图像帧跟踪、系统重置、状态管理和数据记录等关键功能。
- ### *CLASS – VisualSlamSettings*
  - 所属命名空间：realm
  - 继承自：SettingsBase
  - 对应的代码文件：visual_slam_settings.h
  - 说明：定义了一个视觉SLAM接口类VisualSlamIF，其主要目的在于提供一个标准化接口，供不同的视觉SLAM实现使用。它定义了一系列必要的函数和数据结构，包括用于处理图像帧跟踪、系统重置、状态管理和数据记录等关键功能。
- ### *CLASS – OrbSlamSettings、SvoSettings、Svo2Settings、DsoSettings、OpenVslamSettings*
  - 所属命名空间：realm
  - 继承自：[VisualSlamSettings](#class--visualslamsettings)
  - 对应的代码文件：visual_slam_settings.h
  - 说明：不同的视觉SLAM实现。它定义了一系列必要的函数和数据结构，包括用于处理图像帧跟踪、系统重置、状态管理和数据记录等关键功能。
- ### *CLASS – OpenVslam*
  - 所属命名空间：realm
  - 继承自：[VisualSlamIF](#class--visualslamif)
  - 对应的代码文件：open_vslam.h、open_vslam.cpp
  - 说明：实现了可用于视觉SLAM的功能，能够处理图像帧、IMU数据、跟踪相机位置，以及管理关键帧。它的主要功能包括提供跟踪状态、绘制跟踪图像、获取地图点云，并允许系统重置和配置设置的日志记录。
- ### *CLASS – OrbSlam*
  - 所属命名空间：realm
  - 继承自：[VisualSlamIF](#class--visualslamif)
  - 对应的代码文件：rob_slam.h、orb_slam.cpp
  - 说明：实现了对ORB_SLAM的一个功能性抽象，使得通过统一的接口与外部系统（如相机和IMU）进行交互。它的主要功能包括初始化SLAM系统、处理图像帧、管理关键帧、访问地图点云，以及与其他系统进行数据交互。
- ### *CLASS – GeospatialReferencerIF*
  - 所属命名空间：realm
  - 对应的代码文件：geospatial_reference_IF.h
  - 说明：定义了一个用于处理地理空间数据的接口，包含了状态管理、帧处理和变换计算的基本功能。
- ### *CLASS – GeometricReferencer*
  - 所属命名空间：realm
  - 继承自：[GeospatialReferencerIF](#class--geospatialreferencerif)
  - 对应的代码文件：geometric_referencer.h、geometric_referencer.cpp
  - 说明：实现地理空间数据的几何参考。它提供了初始化、更新和转换的核心功能，并具有管理其状态和数据的私有机制。这个类可以用于处理与视觉SLAM相关的应用程序，特别是在进行GIS数据融合时，实现在不同坐标系之间的转换与校准。
- ### *CLASS – DummyReferencer*
  - 所属命名空间：realm
  - 继承自：[GeospatialReferencerIF](#class--geospatialreferencerif)
  - 对应的代码文件：dummy_referencer.h、dummy_referencer.cpp
  - 说明：它是一个地理空间参考器的简单实现。其主要功能包括初始化、获取变换矩阵、更新帧以及检查自身状态，适用于定位或计算相对位置等任务。通过互斥锁，该类具备了线程安全的能力，确保在并发环境下对变换矩阵的安全访问。

---
<br>

# realm_stages
**所在路径：/OpenREALM/modules/realm_vslam/realm_stages** <br>
功能：这个模块是提供了一些处理阶段的类，如拼接，重建，表面生成等。每个阶段都可以独立运行，也可以通过ROS或其他框架进行通信。<br>
链接库：主要使用了EXIV2、OpenCV、PCL、densifier、ortho、vslam_base。<br>
主要有以下几个类：
- ### *CLASS – StageBase*
  - 所属命名空间：realm
  - 继承自：WorkerThreadBase
  - 对应的代码文件：stage_base.h、stage_base.cpp
  - 说明：StageBase 类是所有阶段类的基类。它提供了线程处理、参数更改、统计信息获取等基本功能。
- ### *CLASS – Tileing*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：tileing.h、tileing.cpp
  - 说明：Tileing 类用于处理图像的瓦片化操作。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – SurfaceGeneration*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：surface_generation.h、surface_generation.cpp
  - 说明：SurfaceGeneration 类用于生成表面模型。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – StageSettings*
  - 所属命名空间：realm
  - 继承自：SettingsBase
  - 对应的代码文件：stage_settings.h
  - 说明：StageSettings 类用于定义阶段的设置参数。它继承自 SettingsBase，并添加了一些特定于阶段的参数。
- ### *CLASS – PoseEstimationSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：PoseEstimationSettings 类用于定义姿态估计阶段的设置参数。它继承自 StageSettings，并添加了一些特定于姿态估计的参数。
- ### *CLASS – DensificationSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：DensificationSettings 类用于定义密集化阶段的设置参数。它继承自 StageSettings，并添加了一些特定于密集化的参数。
- ### *CLASS – SurfaceGenerationSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：SurfaceGenerationSettings 类用于定义表面生成阶段的设置参数。它继承自 StageSettings，并添加了一些特定于表面生成的参数。
- ### *CLASS – OrthoRectificationSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：OrthoRectificationSettings 类用于定义正射校正阶段的设置参数。它继承自 StageSettings，并添加了一些特定于正射校正的参数。
- ### *CLASS – MosaicingSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：MosaicingSettings 类用于定义拼接阶段的设置参数。它继承自 StageSettings，并添加了一些特定于拼接的参数。
- ### *CLASS – TileingSettings*
  - 所属命名空间：realm
  - 继承自：[StageSettings](#class--stagesettings)
  - 对应的代码文件：stage_settings.h
  - 说明：TileingSettings 类用于定义瓦片化阶段的设置参数。它继承自 StageSettings，并添加了一些特定于瓦片化的参数。
- ### *CLASS – StageSettingsFactory*
  - 所属命名空间：realm
  - 对应的代码文件：stage_settings_factory.h
  - 说明：StageSettingsFactory 类用于加载阶段设置。它提供了一个静态方法 load，用于从文件中加载特定阶段类型的设置。
- ### *CLASS – OrthoRectification*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：ortho_rectification.h、ortho_rectification.cpp
  - 说明：OrthoRectification 类用于处理正射校正操作。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – Mosaicing*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：mosaicing.h、mosaicing.cpp
  - 说明：Mosaicing 类用于处理图像的拼接操作。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – Densification*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：densification.h、densification.cpp
  - 说明：Densification 类用于处理图像的密集化操作。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – PoseEstimation*
  - 所属命名空间：realm::stages
  - 继承自：[StageBase](#class--stagebase)
  - 对应的代码文件：pose_estimation.h、pose_estimation.cpp
  - 说明：PoseEstimation 类用于处理姿态估计操作。它继承自 StageBase，并实现了图像帧的添加、处理和保存等功能。
- ### *CLASS – PoseEstimationIO*
  - 所属命名空间：realm::stages
  - 继承自：WorkerThreadBase
  - 对应的代码文件：pose_estimation.h、pose_estimation.cpp
  - 说明：PoseEstimationIO 类用于处理姿态估计的输入输出操作。它继承自 WorkerThreadBase，并实现了任务的调度和发布等功能。

---
<br>

# realm_ortho
**所在路径：/OpenREALM/modules/realm_vslam/realm_stages** <br>
功能：主要用于处理与正射影像和地理空间数据相关的操作。它提供了一系列工具和类，用于图像校正、瓦片切割、DSM生成、最近邻搜索等功能。该模块依赖于GDAL库进行地理空间数据的处理，并使用了OpenCV和Eigen库进行图像和矩阵操作。<br>
链接库：主要使用了OpenCV、GDAL、CGAL。<br>
主要有以下几个类：
- ### *CLASS – Tile*
  - 所属命名空间：realm
  - 对应的代码文件：tile.h、tile.cpp
  - 说明：Tile 类是一个容器类，定义了特定缩放级别下的坐标 (x, y) 和包含数据的多层网格地图。它提供了锁定和解锁功能以防止多线程访问问题，并包含获取缩放级别、x 和 y 方向的瓦片索引以及数据的方法。
- ### *CLASS – TileCache*
  - 所属命名空间：realm
  - 继承自：WorkerThreadBase
  - 对应的代码文件：tile_cache.h、tile_cache.cpp
  - 说明：TileCache 类用于缓存瓦片数据。它提供了添加、获取瓦片的方法，并支持将缓存的数据写入磁盘或从磁盘加载。它还包含一些内部结构体用于管理缓存元素和图层元数据。
- ### *CLASS – GdalWarper*
  - 所属命名空间：realm::gis
  - 对应的代码文件：gdal_warper.h、gdal_warper.cpp
  - 说明：GdalWarper 类使用 GDAL 库将输入的 CvGridMap 从 UTM 坐标转换为 EPSG 标准坐标系。它支持设置目标 EPSG 代码和使用的线程数，并提供了将栅格数据进行投影转换的方法。
- ### *CLASS – DigitalSurfaceModel*
  - 所属命名空间：realm::ortho
  - 对应的代码文件：dsm.h、dsm.cpp
  - 说明：DigitalSurfaceModel 类用于创建数字表面模型。它支持平面和高程表面，提供了从点云数据计算高程网格的方法，并支持多种表面法线计算模式。
- ### *CLASS – Delaunay2D*
  - 所属命名空间：realm
  - 对应的代码文件：delaunay_2d.h、delaunay_2d.cpp
  - 说明：Delaunay2D 类用于在二维平面上构建 Delaunay 三角网格。它提供了从 CvGridMap 构建网格的方法，并支持使用掩码进行过滤。
- ### *CLASS – MapTiler*
  - 所属命名空间：realm
  - 对应的代码文件：map_tiler.h、map_tiler.cpp
  - 说明：MapTiler 类用于将地理参考的 CvGridMap 切片成不同缩放级别的等大小瓦片。它提供了创建瓦片的方法，并包含一些实用函数用于坐标转换和瓦片边界计算。
- ### *CLASS – Rectification*
  - 所属命名空间：realm::ortho
  - 对应的代码文件：rectification.h、rectification.cpp
  - 说明：Rectification 类提供了简化的接口函数用于图像校正。它包含一个函数用于将航测数据进行校正，并提供了一个内部函数用于计算高程角度。
- ### *CLASS – NearestNeighbor*
  - 所属命名空间：realm::ortho
  - 对应的代码文件：nearest_neighbor.h
  - 说明：NearestNeighbor 类提供了一个自定义数据集类和一个适配器类，用于将点云数据转换为 kd-tree。它包含一些用于 kd-tree 搜索的辅助函数和结构体。
- ### *CLASS – Nanoflann*
  - 所属命名空间：realm::ortho::nanoflann
  - 对应的代码文件：nanoflann.h
  - 说明：Nanoflann 类是一个 C++ 头文件库，用于构建 KD-Tree，主要优化用于 2D 或 3D 点云。它包含了一些结果集类、度量类和 KD-Tree 类，用于最近邻搜索和距离计算。
