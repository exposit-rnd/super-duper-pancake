# Экосистема: NVIDIA

Важные заметки:

* [`Архитектуры GPU карт и грейды вычислительной мощности`](https://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/) Важно понимать, что у разных поколений карт значительная разница в архитектуре и мощности. Многие продукты будут работать только с определённой архитектурой.

## Общие ссылки и технологии

* [**`Solutions & Industries`**](https://developer.nvidia.com/solutions-and-industries) Главная страница с разбиением на технологии и индустрии.
* [`Deep Learning Institute`](https://www.nvidia.com/en-us/training/) Платформа с обучающими материалами Nvidia по DL тематике.
  * [**`Self-Paced Online Training`**](https://www.nvidia.com/en-us/training/online/) Список доступных курсов для изучения.
  * [`Educator Programs`](https://www.nvidia.com/en-us/training/educator-programs/) Обучающие программы с воркшопами для студентов.
* [`Deep Learning SDK`](https://developer.nvidia.com/deep-learning-software) Список основных SDK от Nvidia для работы с DL.
* [**`CUDA Toolkit`**](https://developer.nvidia.com/cuda-toolkit) Окружение разработки для работы с графическими ускорителями Nvidia.
* [`CUDA Python`](https://developer.nvidia.com/cuda-python) Cython & Python обёртка для вызова CUDA функций и работы с CUDA driver/runtime API.
* [`CUDA-X`](https://developer.nvidia.com/gpu-accelerated-libraries) Документация по коллекции CUDA библиотек, инструментов и технологий с поддержкой аппаратного ускорения. В коллекцию входят библиотеки для работы с изображениями, видео, математическими - тензорными операциями и т.д.
* [**`Download Center`**](https://developer.nvidia.com/gameworksdownload) Архив ссылок на все продукты компании.

## [**HPC**: High-Performance Computing](https://developer.nvidia.com/hpc)

### Tools & Ecosystem

* [**`HPC SDK`**](https://developer.nvidia.com/hpc-sdk) C, C++, Fortran компиляторы и набор библиотек для работы с самыми различными математическими задачами на GPU. Лучше читать подробней самому.
* [`OpenCL`](https://developer.nvidia.com/opencl)
* [`IndeX® 3D`](https://developer.nvidia.com/nvidia-index)

### Models Tools

* [**`Nsight Deep Learning Designer`**](https://developer.nvidia.com/nsight-dl-designer) IDE для дизайна и работы с DL моделями, инференса, профайлинга, сбора метрик, анализа моделей. Обязательное требование: [sm70+](https://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/).

### Performance Analysis Tools

Поставляются вместе с [CUDA](https://developer.nvidia.com/cuda-downloads).

* [`Nsight Systems`](https://developer.nvidia.com/nsight-systems) Низкоуровневый визуальный мониторинг аппаратной загруженности при работе с приложениями. Позволяет определить наилучшие возможности для оптимизации приложения.
* [**`Nsight Compute`**](https://developer.nvidia.com/nsight-compute) Интерактивный kernel профайлер для CUDA приложений.
* [**`Feature Map Explorer`**](https://developer.nvidia.com/nvidia-fme) FME позволяет визуализировать четырехмерные данные feature map на основе изображений с использованием различных фильтров, от визуализации каналов низкого уровня до подробной числовой информации о полном тензоре карты признаков и каждом срезе канала.
* [`DCGM`](https://developer.nvidia.com/dcgm) Мониторинг датацентров с кластерами видеокарт Nvidia. Health мониторинг, диагностика загрузки, системные нотификации.

## [Deep Learning](https://developer.nvidia.com/deep-learning)

### [Frameworks](https://developer.nvidia.com/deep-learning-frameworks)

Список поддерживаемых фреймворков и платформ со всеми нужными ссылками, категориями моделей в NGC и дополнительными ресурсами.

### [Technologies](https://developer.nvidia.com/deep-learning-software)

#### Training

* [**`Data Loading Library (DALI)`**](https://github.com/NVIDIA/dali) Библиотека с GPU-ускорением загрузки и аугментации данных, построения пайплайнов на Python.
* [`NVIDIA Collective Communications Library (NCCL)`](https://developer.nvidia.com/nccl) Библиотека для работы с кластерами видеокарт и распределения процессов обучения и инференса.
* [`NVIDIA Neural Modules (NeMo)`](https://github.com/NVIDIA/NeMo) Инструментарий для построения нейронных моделей с примерами, нацеленными на NLP.
* [**`TAO Toolkit`**](https://developer.nvidia.com/tao-toolkit) Python инструментарий для оптимизации предтренированных нейронных моделей. Раньше назывался Transfer Learning Toolkit.
* [`DIGITS`](https://developer.nvidia.com/digits) Интерактивный инструментарий для работы с CV моделями и обучения классических CV задач.


#### Inference

* [**`TensorRT`**](https://developer.nvidia.com/tensorrt)
* [**`DeepStream SDK`**](https://developer.nvidia.com/deepstream-sdk)
* [**`Triton Inference Server`**](https://developer.nvidia.com/nvidia-triton-inference-server)

#### Development

[Nsight Systems](https://developer.nvidia.com/nsight-systems), [Nsight Compute](https://developer.nvidia.com/nsight-compute), [Kubernetes on NVIDIA GPUs](https://developer.nvidia.com/kubernetes-gpu), [Feature Map Explorer](https://developer.nvidia.com/nvidia-fme)

### [Examples](https://developer.nvidia.com/deep-learning-examples)

[**NGC | NVIDIA GPU Cloud**](https://catalog.ngc.nvidia.com/) Платформа с обученными и оптимизированными моделями под все поддерживаемые фреймворки, Docker контейнерами, Helm Charts и прочими ресурсами.

## [NVIDIA Maxine](https://developer.nvidia.com/maxine) - VIDEO & AUDIO SOTA SDK

SDK с набором SOTA моделей и технологий, который позволяет разработчикам создавать приложения для виртуальной совместной работы и создания контента, такие как видеоконференции и потоковое вещание.

Основные направления:

* **Video Effects**: Super resolution, upscaler, artifact reduction, video noise removal, virtual background.
* **Augmented Reality**: Face detection, mesh, keypoints, body pose estimation, eye contact, audio2face.
* **Audio Effects**: Noise removal, room echo removal, audio super resolution, acoustic echo cancellation.

Технические требования **SM70+**:
*Windows SDK: NVIDIA® GeForce RTX® 20XX and 30XX Series, Quadro RTX™ 3000, TITAN RTX™, or higher (any NVIDIA GPUs with Tensor Cores) Server SDK: V100, T4, A10, A30, A100 (with MIG support)*

## [NVIDIA Clara](https://developer.nvidia.com/clara) - HEALTHCARE AND LIFE SCIENCES