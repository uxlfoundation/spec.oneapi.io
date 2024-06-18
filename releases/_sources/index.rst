.. SPDX-FileCopyrightText: 2021 Intel Corporation
..
.. SPDX-License-Identifier: CC-BY-4.0

===============================
 oneAPI Specification Releases
===============================


This document lists releases of oneAPI specifications.

In addition to be published as part of the oneAPI spefication, some of
the components publish specifications independent from the oneAPI
specification. Typically, a oneAPI specification includes a snapshot
of the latest approved release of the component. This page lists
releases of the oneAPI specification and releases of component
specifications.  Releases of collections of oneAPI components
(e.g. Intel oneAPI Basekit) identify the version of the oneAPI
specification that it supports.


oneAPI Specification
====================

Releases are listed below. See GitHub_ for the latest build.

.. _GitHub: https://github.com/oneapi-src/oneapi-spec


1.3
---

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `1.3 rev 1`_
    - 2023-11-06
    - `HTML <https://spec.oneapi.io/versions/1.3-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.3-rev-1/oneAPI-spec.pdf>`__
  * - `1.3 provisional rev 1`_
    - 2023-9-14
    - `HTML <https://spec.oneapi.io/versions/1.3-provisional-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.3-provisional-rev-1/oneAPI-spec.pdf>`__

1.2
---

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `1.2 rev 1`_
    - 2022-11-10
    - `HTML <https://spec.oneapi.io/versions/1.2-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.2-rev-1/oneAPI-spec.pdf>`__
  * - `1.2 provisional rev 1`_
    - 2022-9-8
    - `HTML <https://spec.oneapi.io/versions/1.2-provisional-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.2-provisional-rev-1/oneAPI-spec.pdf>`__

1.1
---

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `1.1 rev 1`_
    - 2021-11-12
    - `HTML <https://spec.oneapi.io/versions/1.1-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.1-rev-1/oneAPI-spec.pdf>`__
  * - `1.1 provisional rev 2`_
    - 2021-7-19
    - `HTML <https://spec.oneapi.io/versions/1.1-provisional-rev-2/>`__ `PDF <https://spec.oneapi.io/versions/1.1-provisional-rev-2/oneAPI-spec.pdf>`__
  * - `1.1 provisional rev 1`_
    - 2021-4-7
    - `HTML <https://spec.oneapi.io/versions/1.1-provisional-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.1-provisional-rev-1/oneAPI-spec.pdf>`__


1.0
---

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `1.0 rev 2`_
    - 2020-10-21
    - `HTML <https://spec.oneapi.io/versions/1.0-rev-2/>`__ `PDF <https://spec.oneapi.io/versions/1.0-rev-2/oneAPI-spec.pdf>`__
  * - `1.0 rev 1`_
    - 2020-9-14
    - `HTML <https://spec.oneapi.io/versions/1.0-rev-1/>`__ `PDF <https://spec.oneapi.io/versions/1.0-rev-1/oneAPI-spec.pdf>`__

Release Notes
-------------

1.3 rev 1
~~~~~~~~~

Changes since 1.2

* oneDPL

  * Specified how random number generators and distributions support
    sycl::vec
  * Incremental improvements and fixes

* oneCCL

  * For oneCCL, we added new APIs for point to point send/recv
    operations.
    
* Level Zero

  See `Level Zero`_
  
* oneTBB

  * Allowed using pointers to class functions and members in place of
    function objects
  * Incremental improvements and fixes, including fixes in the oneTBB
    named requirements

* oneMKL

  * Introduced RNG Device API
  * Added complex version of BLAS SYR/SYR2/SYMV
  * Added optional index_base parameter for BLAS IAMAX/IAMIN
  * Allow either values or pointers for scalar parameters to BLAS
    functions with USM interfaces
  * Added DFT move/copy constructor/assignment to descriptor class
  * Added forward/backward strides to DFT API
  * Added SYCL queue to Sparse BLAS matrix handle initialization API
  * Added NNZ argument to Sparse BLAS set_csr_data API
  * Fixed bugs

1.3 provisional rev 1
~~~~~~~~~~~~~~~~~~~~~

1.2 rev 1
~~~~~~~~~

Changes since 1.1

* SYCL

  The following extensions were added:
  
  * `sycl_ext_oneapi_assert` - Support for device-side assert.
  * `sycl_ext_oneapi_default_context` - Adds the concept of a platform
    default context.
  * `sycl_ext_oneapi_discard_queue_events` - Adds a queue property
    that can optimize queues in some circumstances.
  * `sycl_ext_oneapi_srgb` - Exposes sRGB support for images.
  * `sycl_ext_oneapi_usm_device_read_only` - Adds a property for USM
    allocations.
  
* oneDPL

  The following updates were added in oneDPL specification for version 1.2:
  
  * The content was reorganized.
  * API for random number generation was added.
  * Incremental improvements and bug fixes.
  
* oneDNN

  This is a new major release of oneDNN spec, which breaks
  compatibility with previously published versions.

  * oneDNN Graph extension: a graph extension is added to allow
    seamless fusion of operations, and more flexibility for backend
    specific optimizations.
  * reworked quantization workflow: in order to support dynamic
    quantization efficiently and allow better reuse of primitive
    objects, quantization parameters are no longer passed at primitive
    creation, but at primitive execution.  This also allows to pass
    quantization parameters from device memory, instead of passing
    them from host memory.
  * opaque memory descriptors, and removal of operation descriptors:
    this allows more flexibility for oneDNN implementation to add new
    memory layouts and primitive extensions without breaking
    compatibility.
  * Better support for type conversion fusion: all primitives now take
    separate descriptors for input and output, which allows to fuse
    type conversions to all primitives.

* Level Zero

  See `Level Zero`_
  
* oneTBB

  The following updates were added in oneTBB specification for version
  1.2:
  
  * Support for core types and thread-per-core limit was added to
    task_arena constraints.
  * API of concurrent_queue and concurrent_bounded_queue was extended
    to better match C++ standard containers.
  * Incremental improvements and bug fixes.
  
* oneVPL

  This release updates oneVPL specification to version 2.9.0. New
  features include:
  
  * Deprecated mfxExtCodingOption2::BitrateLimit.
  * Added note that applications must call MFXVideoENCODE_Query() to
    check for support of mfxExtChromaLocInfo and mfxExtHEVCRegion
    extension buffers.
  * Added AV1 HDR metadata description and further clarified
    mfxExtMasteringDisplayColourVolume and
    mfxExtContentLightLevelInfo.
  * Added deprecation messages to the functions MFXQueryAdapters,
    MFXQueryAdaptersDecode, and MFXQueryAdaptersNumber.
    Applications should use the process described in oneVPL Dispatcher
    to enumerate and select adapters.
  * Fixed multiple spelling errors.
  * Added extension buffer mfxExtSyncSubmission to return submission
    synchronization sync point.
  * Added extension buffer mfxExtVPPPercEncPrefilte to control
    perceptual encoding prefilter.
  * Deprecated mfxPlatform::CodeName and corresponding enum values.
  * Added mfxExtendedDeviceId::RevisionID and extDeviceUUID to be
    aligned across multiple domains including compute and specify device
    UUID accordingly.
  * Added extension buffer mfxExtTuneEncodeQuality and correspondent
    enumeration to specify encoding tuning option.
  * Updated description of MFXEnumImplementations to clarify that the
    input mfxImplCapsDeliveryFormat determines the type of structure returned.
  * Updated mfxvideo++.h to use MFXLoad API.

* oneMKL

  The following updates were added in oneMKL specification for version
  1.2:
  
  * Dense matrix copy and transpose routines were added in the
    BLAS-like extensions
  * half/bfloat16 precision support were added to several L1 BLAS
    routines
  * The supported precisions for BLAS gemm and gemm_batch were updated
  * Several routines in BLAS had const attributes properly assigned to
    arguments
  * Add a missing constraint on parameter "n" for LAPACK orgqr
    routines
  * Improve directories tree of VM, RNG, Stats domains of oneMKL. Fix
    minor issues in RNG
  * Other changes include minor clarifications and bug fixes.


1.2 provisional rev 1
~~~~~~~~~~~~~~~~~~~~~

1.1 rev 1
~~~~~~~~~

Changes since 1.0

* Ray Tracing: Added

  * Ray tracing capabilities have been added to the oneAPI
    specification providing software developers across the industry
    the ability to “write once” for high-fidelity ray-traced
    computations across multiple vendors’ systems and
    accelerators. Standardizing these interfaces provides
    well-designed, tried and true APIs and options for a broad set of
    compute and rendering infrastructure development.

  * The ray tracing functionality is subdivided into several
    domains within the oneAPI Specification:

    * Geometric ray tracing computations
    * Volumetric computation and rendering
    * Image denoising
    * Scalable rendering and visualization infrastructure

  * The set of Ray Tracing APIs include the following, which
    are in active use via the Intel® oneAPI Rendering Toolkit:

    * Embree
    * Open Volume Kernel Library
    * Open Image Denoise
    * OSPRay

* oneMKL:

  Introduces additional batched APIs for dense linear algebra. Sparse
  matrix-dense matrix product has been extended to support both row
  and column major layout for the dense matrix. The input USM pointers
  in the vector math APIs are now const qualified. To align with
  changes in SYCL 2020, all oneMKL USM APIs were updated to take an
  (optional) std::vector of input events instead of
  sycl::vector_class. Other changes include minor clarifications and
  bug fixes.
  
* oneTBB:

  Introduces a way for collaborative one-time function processing
  (collaborative_call_once), mutex classes with adaptive waiting
  behavior (mutex, rw_mutex), the ability to wait for thread completion
  (task_scheduler_handle and the finalize function). Extended task_group
  and task_arena classes to support deferred task submission via 
  the new task_handle class. Extended concurrent_hash_map with methods
  that support lookup for distinct key types.

* DPC++

  The new extensions listed as part of oneAPI 1.1 include simplified
  device selection through text-based filtering, a default context for
  each platform to simplify common coding patterns, interoperability
  with devices that use Level Zero as a backend, an easier to use
  kernel-scope local memory allocation mechanism, GPU-specific
  information queries, FPGA-specific performance tuning controls, and
  a sub-group mask feature.

  DPC++ features that were incorporated into the SYCL 2020 spec were
  removed from this document.

* oneVPL

  New AV1 encode features. Enabled support for planar I422, I210, and
  BGR formats. Added surface pool interface for surface management.

* Level Zero

  Updates included significantly improved image processing
  functionality, better interoperability with other APIs and operating
  systems, new extensions for floating-point atomics and additional
  subgroup operations, and extensions to tune and optimize the way
  memory is allocated and kernels are scheduled on specific devices.

1.1 provisional rev 2
~~~~~~~~~~~~~~~~~~~~~

* oneVPL: Updated to 2.4.0
* oneDAL: Updated some APIs
* oneMKL: bug fixes

1.1 provisional rev 1
~~~~~~~~~~~~~~~~~~~~~

* Ray Tracing: added to oneAPI specification
* VPL: Updated to 2.3.1
* Level Zero: Updated to 1.1.2
* oneDNN: Added graph API

1.0 rev 2
~~~~~~~~~

* Formatting fixes for PDF

1.0 rev 1
~~~~~~~~~

* Initial release

oneIPL
======

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `oneIPL v0.6`_
    - 2022-02-18
    - `HTML <https://spec.oneapi.io/oneipl/0.6/index.html>`__
  * - `oneIPL v0.5`_
    - 2021-10-8
    - `HTML <https://spec.oneapi.io/oneipl/0.5/index.html>`__


Release Notes
-------------

oneIPL v0.6
~~~~~~~~~~~

* Color coding changed to memory layout in image API
* Image parameters access moved to image API
* Minor API change for gaussian and normalize

oneIPL v0.5
~~~~~~~~~~~

Initial release


oneDTL
======

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `oneDTL v0.5`_
    - 2021-11-10
    - `HTML <https://spec.oneapi.io/onedtl/latest/index.html>`__


Release Notes
-------------

oneDTL v0.5
~~~~~~~~~~~

Initial release


Ray Tracing
===========

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `Ray Tracing v0.5`_
    - 2021-2-18
    - `HTML <https://spec.oneapi.io/oneart/0.5-rev-1/index.html>`__


Release Notes
-------------

Ray Tracing v0.5
~~~~~~~~~~~~~~~~

* Ray tracing capabilities have been added to the oneAPI
  specification providing software developers across the industry the
  ability to “write once” for high-fidelity ray-traced computations
  across multiple vendors’ systems and accelerators. Standardizing
  these interfaces provides well-designed, tried and true APIs and
  options for a broad set of compute and rendering infrastructure
  development.

* The ray tracing functionality is subdivided into several
  domains within the oneAPI Specification:

  * Geometric ray tracing computations
  * Volumetric computation and rendering
  * Image denoising
  * Scalable rendering and visualization infrastructure

* The set of Ray Tracing APIs include the following, which
  are in active use via the Intel® oneAPI Rendering Toolkit:

  * Embree
  * Open Volume Kernel Library
  * Open Image Denoise
  * OSPRay


oneDNN Graph
============

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `oneDNN Graph v1.0-beta`_
    - 2022-10-14
    - `HTML <https://spec.oneapi.io/onednn-graph/v1.0-beta/index.html>`__
  * - `oneDNN Graph v1.0-alpha`_
    - 2021-04-01
    - `HTML <https://spec.oneapi.io/onednn-graph/v1.0-alpha/index.html>`__
  * - `oneDNN Graph v0.9`_
    - 2021-12-28
    - `HTML <https://spec.oneapi.io/onednn-graph/latest/index.html>`__
  * - `oneDNN Graph v0.8`_
    - 2021-11-8
    - `HTML <https://spec.oneapi.io/onednn-graph/latest/index.html>`__
  * - `oneDNN Graph v0.5`_
    - 2021-4-8
    - `HTML <https://spec.oneapi.io/onednn-graph/latest/index.html>`__

Release Notes
-------------

oneDNN Graph v1.0-beta
~~~~~~~~~~~~~~~~~~~~~~~

- Introduced support for floating point math mode at graph
  construction phase.
- Added finalize API to indicate that the user has finished adding
  operations into the graph and the graph is ready for partitioning.
- Added operations AbsBackprop, Mish, MishBackprop, and LeakyReLU.
- Removed operations HardTanh, Index, Pow, etc.

oneDNN Graph v1.0-alpha
~~~~~~~~~~~~~~~~~~~~~~~

- Introduced FP32 and BF16 training support on CPU

oneDNN Graph v0.9
~~~~~~~~~~~~~~~~~

- Introduced bf16 inference support.
- Introduced multi-head attention (MHA) fusion supported by oneDNN
  Graph compiler with optimized code generation (experimental).

oneDNN Graph v0.8
~~~~~~~~~~~~~~~~~

- Introduces int8 inference support.

oneDNN Graph v0.5
~~~~~~~~~~~~~~~~~

Provides more optimization and improves the programming
experience. The main changes are as follows:

- Support in-place optimization to reduce memory footprint and provide
  better data locality
- Support using the partition vector directly for compilation and
  execution without maintaining a computation graph
- Provide a special End op to express the multiple uses of a logical
  tensor, typically for indicating the output tensors of the graph

oneVPL
======

VPL is no longer part of oneAPI specification. See `VPL
documentation`_ for new releases.

.. _`VPL documentation`: https://intel.github.io/libvpl/latest/index.html

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `oneVPL v2.9.0`_
    - 2023-3-31
    - `HTML <https://spec.oneapi.io/onevpl/2.9.0/index.html>`__
  * - `oneVPL v2.8.0`_
    - 2022-11-1
    - `HTML <https://spec.oneapi.io/onevpl/2.8.0/index.html>`__
  * - `oneVPL v2.7.1`_
    - 2022-04-01
    - `HTML <https://spec.oneapi.io/onevpl/2.7.1/index.html>`__
  * - `oneVPL v2.7.0`_
    - 2022-3-10
    - `HTML <https://spec.oneapi.io/onevpl/2.7.0/index.html>`__
  * - `oneVPL v2.6.0`_
    - 2021-12-3
    - `HTML <https://spec.oneapi.io/onevpl/2.6.0/index.html>`__
  * - `oneVPL v2.5.0`_
    - 2021-8-30
    - `HTML <https://spec.oneapi.io/onevpl/2.5.0/index.html>`__
  * - `oneVPL v2.4.0`_
    - 2021-5-12
    - `HTML <https://spec.oneapi.io/onevpl/2.4.0/index.html>`__
  * - `oneVPL v2.3.1`_
    - 2021-4-8
    - `HTML <https://spec.oneapi.io/onevpl/2.3.1/index.html>`__

Release Notes
-------------

oneVPL v2.9.0
~~~~~~~~~~~~~

* Deprecated mfxExtCodingOption2::BitrateLimit.
* Added note that applications must call MFXVideoENCODE_Query() to
  check for support of mfxExtChromaLocInfo and mfxExtHEVCRegion
  extension buffers.
* Added AV1 HDR metadata description and further clarified
  mfxExtMasteringDisplayColourVolume and
  mfxExtContentLightLevelInfo.
* Added deprecation messages to the functions MFXQueryAdapters,
  MFXQueryAdaptersDecode, and MFXQueryAdaptersNumber.
  Applications should use the process described in oneVPL Dispatcher
  to enumerate and select adapters.
* Fixed multiple spelling errors.
* Added extension buffer mfxExtSyncSubmission to return submission
  synchronization sync point.
* Added extension buffer mfxExtVPPPercEncPrefilte to control
  perceptual encoding prefilter.
* Deprecated mfxPlatform::CodeName and corresponding enum values.
* Added mfxExtendedDeviceId::RevisionID and extDeviceUUID to be
  aligned across multiple domains including compute and specify device
  UUID accordingly.
* Added extension buffer mfxExtTuneEncodeQuality and correspondent
  enumeration to specify encoding tuning option.
* Updated description of MFXEnumImplementations to clarify that the
  input mfxImplCapsDeliveryFormat determines the type of structure returned.
* Updated mfxvideo++.h to use MFXLoad API.

oneVPL v2.8.0
~~~~~~~~~~~~~

New in this release:

* Introduced MFX_FOURCC_ABGR16F FourCC for 16-bit float point (per
  channel) 4:4:4 ABGR format.
* Clarified the mfxExtMasteringDisplayColourVolume::DisplayPrimariesX,
  mfxExtMasteringDisplayColourVolume::DisplayPrimariesY for the video
  processing usage.
* Added MFX_CONTENT_NOISY_VIDEO in ContentInfo definition.
* Added Camera Processing API for Camera RAW data.
* Introduced hint to disable external video frames caching for GPU copy.
* Clarified usage of
  mfxExtMasteringDisplayColourVolume::InsertPayloadToggle and
  mfxExtContentLightLevelInfo::InsertPayloadToggle during decode
  operations.
* Fixed multiple spelling errors.
* Experimental API: introduced mfxExtMBQP::Pitch value for QP map
  defined in mfxExtMBQP.
* Clarified when MFXEnumImplementations() may be called for
  implementation capabilities query.
* Added table with filenames included in the dispatcher’s search
  process.

Bug Fixes:

* Fixed Experimental API table to note that mfxExtRefListCtrl and
  MFX_EXTBUFF_UNIVERSAL_REFLIST_CTRL were moved to production in
  version 2.8.

oneVPL v2.7.1
~~~~~~~~~~~~~

Bug Fixes:

* changed use of word "interface" in header to avoid conflict with
  MSVC reserved words.

oneVPL v2.7.0
~~~~~~~~~~~~~

New in this release:

* mfxExtVppAuxData::RepeatedFrame flag has been un-deprecated.
* Clarified GPUCopy control behavior.
* Introduced MFX_FOURCC_XYUV FourCC for non-alpha packed 4:4:4 format.
* Notice added to the mfxFrameSurfaceInterface::OnComplete to clarify
  when library can call this callback.
* Annotated missed aliases mfxExtHEVCRefListCtrl, mfxExtHEVCRefLists,
  mfxExtHEVCTemporalLayers.
* Refined description of mfxExtMasteringDisplayColourVolume and
  mfxExtContentLightLevelInfo for HDR SEI decoder usage.
* Experimental API: introduced interface to get statistics after
  encode.
* New dispatcher config properties:

    * Pass through extension buffer to mfxInitializationParam.
    * Select host or device responsible for the memory copy between
      host and device.

Bug Fixes:

* Fixed misprint in mfxExtDeviceAffinityMask description.
* MFXVideoENCODE_Query description fixed for query mode 1.

oneVPL v2.6.0
~~~~~~~~~~~~~

New in this release:

* New development practice to treat some new API features as
  experimental was introduced.
  All new experimental API is wrapped with ONE_EXPERIMENTAL macro.
* Experimental API: introduced MFX_HANDLE_PXP_CONTEXT to support
  protected content.
* Experimental API: introduced CPUEncToolsProcessing hint to run
  adaptive encoding tools on CPU.
* Experimental API: extended device ID reporting to cover
  multi-adapter cases.
* Experimental API: introduced common alias for mfxExtAVCRefListCtrl
* Experimental API: mfxExtDecodeErrorReport ErrorTypes enum extended
  with new JPEG/MJPEG decode error report.
* Clarified LowPower flag meaning.
* Described that mfxExtThreadsParam can be attached to
  mfxInitializationParam during session initialization.
* Refined description of the MFXVideoDECODE_VPP_DecodeFrameAsync
  function.
* New dispatcher's config filter property: MediaAdapterType.
* Marked all deprecated fields as MFX_DEPRECATED.
* Introduced priority loading option for custom libraries.
* Clarified AV1 encoder behavior about writing of IVF headers.
* Removed outdated note about loading priority of Intel Media Software
  Development Kit
* Spelled out mfxVariant type usage for strings.
* New product names for platforms:

    * Code name DG2,
    * Code name ATS-M.

oneVPL v2.5.0
~~~~~~~~~~~~~

New in this release:

* Added mfxMediaAdapterType to capability reporting.
* Added surface pool interface.
* Helper macro definition to simplify filter properties set up process
  for dispatcher.
* Added mfxExtAV1BitstreamParam, mfxExtAV1ResolutionParam and
  mfxExtAV1TileParam for AV1e.
* Added MFX_RESOURCE_VA_SURFACE_PTR and MFX_RESOURCE_VA_BUFFER_PTR
  enumerators.
* Clarified HEVC Main 10 Still Picture Profile configuration.
* External Buffer ID of mfxExtVideoSignalInfo and
  mfxExtMasteringDisplayColourVolume for video processing.
* New MFX_WRN_ALLOC_TIMEOUT_EXPIRED return status. Indicates that all
  surfaces are currently in use and timeout set by
  mfxExtAllocationHints for allocation of new surfaces through
  functions GetSurfaceForXXX expired.
* Introduced universal temporal layering structure.
* Added MFX_RESOURCE_VA_SURFACE_PTR and MFX_RESOURCE_VA_BUFFER_PTR
  enumerators.
* Introduced segmentation interface for AV1e, including ext-buffers
  and enums.
* Introduced planar I422 and I210 FourCC codes.

Bug Fixes:

* Dispatcher: Removed /etc/ld.so.cache from oneVPL search order.
* mfxSurfaceArray: CDECL attribute added to the member-functions.

Deprecated:

* mfxExtVPPDenoise extension buffer.

oneVPL v2.4.0
~~~~~~~~~~~~~

* Added ability to retrieve path to the shared library with the
  implementation.
* Added 3DLUT (Three-Dimensional Look Up Table) filter in VPP.
* Added mfxGUID structure to specify Globally Unique Identifiers
  (GUIDs).
* Added QueryInterface function to mfxFrameSurfaceInterface.
* Added AdaptiveRef and alias for ExtBrcAdaptiveLTR.
* Added MFX_FOURCC_BGRP FourCC for Planar BGR format.
* Environmental variables to control dispatcher's logger.

oneVPL v2.3.1
~~~~~~~~~~~~~

* Encoding in Hyper mode.

* New product names for platforms:

  * Code name Rocket Lake,
  * Code name Alder Lake S,
  * Code name Alder Lake P,
  * Code name Arctic Sound P.

* mfx.h header file is added which includes all header files.
* Added deprecation messages (deprecation macro) to the MFXInit and
  MFXInitEx functions definition.

Level Zero
==========

.. list-table::
  :widths: 30 20 50
  :header-rows: 1

  * - Version
    - Date
    - View
  * - `Level Zero v1.9.3`_
    - 2024-05-03
    - `HTML <https://spec.oneapi.io/level-zero/1.9.3/index.html>`__  
  * - `Level Zero v1.9.2`_
    - 2024-02-20
    - `HTML <https://spec.oneapi.io/level-zero/1.9.2/index.html>`__
  * - `Level Zero v1.9.1`_
    - 2024-02-09
    - `HTML <https://spec.oneapi.io/level-zero/1.9.1/index.html>`__
  * - `Level Zero v1.9.0`_
    - 2024-02-02
    - `HTML <https://spec.oneapi.io/level-zero/1.9.0/index.html>`__
  * - `Level Zero v1.8.0`_
    - 2023-10-13
    - `HTML <https://spec.oneapi.io/level-zero/1.8.0/index.html>`__
  * - `Level Zero v1.7.8`_
    - 2023-8-28
    - `HTML <https://spec.oneapi.io/level-zero/1.7.8/index.html>`__
  * - `Level Zero v1.7.0`_
    - 2023-7-9
    - `HTML <https://spec.oneapi.io/level-zero/1.7.0/index.html>`__
  * - `Level Zero v1.6.10`_
    - 2023-5-19
    - `HTML <https://spec.oneapi.io/level-zero/1.6.10/index.html>`__
  * - `Level Zero v1.6.3`_
    - 2023-4-25
    - `HTML <https://spec.oneapi.io/level-zero/1.6.3/index.html>`__
  * - `Level Zero v1.6.0`_
    - 2023-3-31
    - `HTML <https://spec.oneapi.io/level-zero/1.6.0/index.html>`__
  * - `Level Zero v1.5.17`_
    - 2023-3-2
    - `HTML <https://spec.oneapi.io/level-zero/1.5.17/index.html>`__
  * - `Level Zero v1.5.16`_
    - 2023-2-28
    - `HTML <https://spec.oneapi.io/level-zero/1.5.16/index.html>`__
  * - `Level Zero v1.5.8`_
    - 2023-1-19
    - `HTML <https://spec.oneapi.io/level-zero/1.5.8/index.html>`__
  * - `Level Zero v1.5.0`_
    - 2023-1-11
    - `HTML <https://spec.oneapi.io/level-zero/1.5.0/index.html>`__
  * - `Level Zero v1.4.8`_
    - 2022-07-22
    - `HTML <https://spec.oneapi.io/level-zero/1.4.8/index.html>`__
  * - `Level Zero v1.4`_
    - 2022-05-05
    - `HTML <https://spec.oneapi.io/level-zero/1.4.0/index.html>`__
  * - `Level Zero v1.3`_
    - 2021-11-27
    - `HTML <https://spec.oneapi.io/level-zero/1.3.7/index.html>`__
  * - `Level Zero v1.2`_
    - 2021-05-11
    - `HTML <https://spec.oneapi.io/level-zero/1.2.43/index.html>`__
  * - `Level Zero v1.1`_
    - 2021-02-04
    - `HTML <https://spec.oneapi.io/level-zero/1.1.2/index.html>`__
  * - `Level Zero v1.0`_
    - 2020-10-02
    - `HTML <https://spec.oneapi.io/level-zero/1.0.4/index.html>`__
  * - `Level Zero v0.95`_
    - 2020-05-28
    - `HTML <https://spec.oneapi.io/level-zero/0.95/index.html>`__
  * - `Level Zero v0.91`_
    - 2020-03-04
    - `HTML <https://spec.oneapi.io/level-zero/0.91/index.html>`__

Release Notes
-------------

Level Zero v1.9.3
~~~~~~~~~~~~~~~~~~

* Patches to v1.9.2 release

    - Misc infrastructure updates 
    - Fix typo in for device property 
    - Update support for sampled bindless images 
    - Update new image formats

Level Zero v1.9.2
~~~~~~~~~~~~~~~~~~

* Patch v1.9 to fix API version enum

Level Zero v1.9.1
~~~~~~~~~~~~~~~~~~

* Misc. patches to v1.9.0 release

    - Add missing enumerations to programming guides
    - Add numWaitEvents parameter to mutable command list update wait events API (needed for loader)
    - Add range to phCommandLists description in append command lists extension
    - Fix spelling error in sysman subdevice properties structure type name
    - Fix immediate command list append API parameter description to work around script limitation
    - Convert fixed-length character array parameters to constant pointers in programmable metrics and firmware secuirty version extensions

Level Zero v1.9.0
~~~~~~~~~~~~~~~~~~

* Core

  - Fix device hierarchy environment variable value in docs
  - Add experimental extension for immediate command list append command lists
  - Add experimental extension to clone a command list
  - Add experimental extension for mutable command lists
  - Add experimental extension for bindless images
  - Add introspection APIs
  - Add invalid argument error code to zeContextMakeMemoryResident

* Sysman

  - Fixes to Memory Bandwidth Extensions
  - Add SURVIVABILITY_MODE_DETECTED event type
  - Clarify engine stats details
  - Add clarification for setting frequency defaults
  - New firmware API for logging
  - Add extension to support Flat device model
  - Add experimental extension to access firmware security version
  - Add experimental extension for VF telemetry

* Tools

  - Add support for programmable metrics

Level Zero v1.8.0
~~~~~~~~~~~~~~~~~~

* Core

  - Add API Versions 1.7, 1.8
  - Add experimental extension for counter-based events
  - Clarify usage of IPC event pools

* Sysman

  - Add RasClearState to extension listing
  - Add MEMORY power domain
  - Add GPU power domain
  - Clarify that the time units for engine activity counters are implementation specific
  - Describe extension discovery
  - Added GPU Board Temperature Metric
  - Add power domain properties extension
  - Deprecate unused APIs and/or APIs with enhanced replacements
  - Deprecate compute unit debug mode
  - Add memory timestamp valid bits experimental extension
  - Add flash progress API
  - Added Memory Page Offline Metrics

Level Zero v1.7.8
~~~~~~~~~~~~~~~~~~

* Core

  - Fix timestamps results parameter attributes

* Sysman

  - Add extension mechanism for dynamically discovering RAS error states
  - Move engine activity extension to separate extension file
  - Add clarifications to board and serial number descriptions
  - Clarify description for multi-port throughput

* Tools

  - Clarify metric streamer desc member descriptions

Level Zero v1.7.0
~~~~~~~~~~~~~~~~~~

* Core

  - Fix a spelling error in the core programming guide command queues section
  - Minor fix to kernel timestamp example in programming guide
  - Some fixes for kernel max group size extension
  - Add clarification to immediate command lists execution
  - Add system memory hint for memory advise
  - Add API to set atomic properties of a shared allocation
  - Add support for in-order lists
  - Add support for flexible device hierarchy model
  - Add ray tracing acceleration structure build experimental extension

* Sysman

  - Various updates for engine, fabric, device and memory
  - Added Fabric Error Counters and API
  - Update engine group descriptions
  - Fixes to GetFabricPortMultiThroughput

* Tools

  - Minor formatting fix for metric export data
  - Fix sample code for MetricGroupGetExportDataExp
  - Promote ZET_METRIC_TYPE_IP_EXP out of experimental
  - Fix ZET typo to conform to naming convention

Level Zero v1.6.10
~~~~~~~~~~~~~~~~~~

* Core

  - Clarify documentation on build logs lifetime
  - Set pNext pointer to NULL in programming guide

* Sysman

  - Add support for machine independent calculation for metrics data
  - Update metrics timer resolution to cycle/sec

* Tools

  - Fix html generation of metric export data example code
  - Fix base type for zet_metric_global_timestamps_resolution_exp_t

* Infrastructure (Scripts)

  - Misc. formatting and infrastructure fixes

Level Zero v1.6.3
~~~~~~~~~~~~~~~~~

* Core

  - Import SECURITY.md

* Sysman

  - Revert RAS Category and Fabric API changes, restoring backwards compatibility.

* Infrastructure (Scripts)

  - Update copyright year for publication.

Level Zero v1.6.0
~~~~~~~~~~~~~~~~~

* Core Changes

  - Add zeMemPutIpcHandle and zeEventPoolPutIpcHandle
  - Add helper functions for IPC handle
  - Add zeDriverGetLastResultString
  - Add zeCommandListHostSynchronize
  - Module build option clarification
  - Introduce extension to query normalized kernel event timestamps
  - Clarify image buffers format/layout restrictions

* Sysman

  - Extend the SYSMAN Frequency Domain list to include a MEDIA Domain

* Infrastructure (Scripts)

  - Fixup extension references and substitutions
  - Fixup parser versions (add newer point releases to all_versions)

Level Zero v1.5.17
~~~~~~~~~~~~~~~~~~

* Tool Changes

  - Add missing version to global metrics timestamps extension

Level Zero v1.5.16
~~~~~~~~~~~~~~~~~~

* Core Changes

  - Clarify intended interpretation of 32-bit device id
  - Clarify that zeContextMakeMemoryResident is a cross-platform API
  - Clarify language for pString parameter of zeKernelGetSourceAttributes
  - Add an extension to get the kernel max group size properties
  - Fixup typo in PCI Properties extension example

* Tool Changes

  - Add extension for global metrics timestamps

* Sysman Changes

  - Explicitly state the timestamp unit for the memory bandwidth API
  - Update value of ZES_MAX_RAS_ERROR_CATEGORY_COUNT macro

Level Zero v1.5.8
~~~~~~~~~~~~~~~~~

* Infrastructure (Scripts)

  - Remove nullptr error code from params with mbz trait
  - Fix handling of mbz attributes
  - Fix ze_device_properties_t in samples

Level Zero v1.5.0
~~~~~~~~~~~~~~~~~

* Core Changes

  - Clarify that a context can also be used by sub-devices of devices
  - Add an extension for bfloat16 conversions
  - Relax restriction and allow ipc events with timestamps
  - Add an extension to return the device IP version
  - Move image view extension to standard
  - Fix off-by-one error for maximum memory allocation size
  - Add host support for IPC allocations
  - Add sub-allocations properties extensions
  - Clarify commands in an immediate command list may execute synchronously
  - Add additional default errors
  
* Tool Changes

  - Add a deprecation message for ZET_ENABLE_API_TRACING_EXP

* Sysman Changes

  - RAS Category and Fabric API
  - Remove out-of-date Sysman object hierarchy diagram
  - Mark zesPowerGetLimits and zesPowerSetLimits as deprecated
  - Separate APIs for initializing and enumerating sysman
  - Correct documentation for zesMemoryGetBandwidth


Level Zero v1.4.8
~~~~~~~~~~~~~~~~~

* Core Changes

  - Fix naming for some fabric extension function args.

* Sysman Changes

  - Remove const for _zes_power_limit_ext_desc_t ouput params.
  - Modify zes_power_level_t desc entry.
  - Add missing structure type enums.

Level Zero v1.4
~~~~~~~~~~~~~~~

* Core Changes

  - Fabric Topology Discovery API extension added.
  - Add detail to allocation access capabilities
  - Add an extension to the Core API for obtaining memory BW
  - Add clarifications for printf
  - Add extension for querying device locally unique identifier
  - Fix reordering of stypes
  - Standardize use of desc in SetEccState

Level Zero v1.3
~~~~~~~~~~~~~~~

* Core Changes

  - Add EU count extension.
  - Add clarification that link log may contain unresolved symbols
    after dynamic linking.
  - Add documentation for dynamic linking.
  - Add extension for linkage inspection.
  - Add extension for obtaining PCI BDF address.
  - Clarify programming guide section on command queues & command lists.
  - Correct documentation regarding maxMemoryFillPatternSize.
  - Clarify that pNext should be nullptr as default.
  - Clarify that unsupported structure types in pNext are ignored.
  - Add extension for image copy to/from memory that permits pitch
    within the memory buffer.
  - Add support for sRGB.
  - Clarify that zeInit needs to be called after forking processes.
  - Clarify barrier execution semantics for zeCommandListAppendBarrier.
  - Add an extension for querying image allocation properties.
  - Add an experimental extension to supply compression hints.

* Tools Changes

  - Add experimental extension for calculating multiple metrics.

Level Zero v1.2
~~~~~~~~~~~~~~~

* Core Changes

  - Added alloc flags for device and host initial placement.
  - Fix spec references.
  - Add clarification that SPIR-V import and export linkage types are
    used.
  - Add VPU to ze_device_type_t and ze_init_flags_t.
  - Add -ze-opt-level build option.
  - Add kernel scheduling hints experimental extension.
  - Add extended subgroups extension.
  - Add image view planar extension.
  - Add image view extension.
  - Add additional kernel preferred group size properties.
  - Add SPIR-V extension for linkonce-odr.
  - Add cache biasing flags for IPC handles.
  - Add documentation pages for extensions.
  - Add kernel scheduling hints for thread arbitration policy.
  - Add image memory properties experimental extension.
  - Add Event Query Timestamps experimental extension.
  - Fix compatibility issue device time resolution.
  - Add RGBP and BRGP image formats.

* Sysman

  - New return codes for low power state.

Level Zero v1.1
~~~~~~~~~~~~~~~

* Core Changes

  - Add code example for interop sharing, importing Linux dma_buf as
    an external memory handle for device allocation.
  - Clarify zeInit behavior regarding multiple calls with different
    flags or environment variables.
  - Add experimental extension for global work offset property to be
    set on kernel.
  - Update timeResolution units to double in device properties.
  - Added zeDeviceGetGlobalTimestamps to return synchronized host and
    device global timestamps.
  - Clarification on non-standard extensions via
    zeDriverGetExtensionFunctionAddress.
  - Clarifications for execution behavior for submitting multiple
    command lists
  - Add zeContextCreateEx to support context visibility for one or
    more device objects.
  - Specify that kernel state is not stored in thread-local storage by
    implementation.
  - Add float atomics extension to support additional floating point
    atomics capabilities.
  - Add extension to relax allocation limits and allow for allocations
    > 4GB.

* Sysman

  - Fix bug in fan spec. The fan configuration zes_fan_config_t should
    point to the table structure zes_fan_table_t instead of one
    temp/speed pair.

* Tools

  - Add page fault debug event ZE_DEBUG_EVENT_TYPE_PAGE_FAULT.
  - Clarification for metric group properties.
  - Remove phWaitEvents parameters from zetCommandListAppendMetricQueryEnd.
  
Level Zero v1.0
~~~~~~~~~~~~~~~

* Core Changes

  - Update command queue group properties to indicate numQueues is
    number of physical engines.
  - Clarify 'Get' parameters such that the pCount description is more
    clear to what is return in array.
  - Clarify metrics flag in ze_command_queue_group_property_flags_t.
  - Fix API documentation to indicate that pIpcProperties argument is
    [in,out] for GetIpcProperties.
  - Add experimental extension "ze_experimental_module_program" to
    support compiling and linking multiple SPIR-V modules together.
  - Updates to Raytracing extension.
  - Clean up Introduction documentation to remove reference to CSA and
    update ABI compatibility.
  - Fix PG documentation error for -g build flag in Module Build
    Options section.
  - Clarify in PG the default signal / wait event behavior.
  - Add cooperative kernel launch code snippet in PG.
  - Clarify that app must ensure the location in the pool is not being
    used by another event in zeEventCreate.

* Sysman

  - Update PG to describe that both min and max temperatures across
    sensors will be included in temp components.
  - Clarify fan configuration comment to indicate that fan temp/speeds
    are passed back as table.
  - Fixed comment showing how to calculate %allocated and %free memory
    in memory state structure.
  - Clean up ambiguous comments in the function and structures for
    scheduler and memory components.

* Tools

  - Fix wrong type in pseudo-code for API Tracing documentation.

Level Zero v0.95
~~~~~~~~~~~~~~~~

* Updates from implementation team.

Level Zero v0.91
~~~~~~~~~~~~~~~~

* Initial release
