# Changelog

## 0.1.0-alpha.1 (2025-04-01)

Full Changelog: [v0.0.1-alpha.0...v0.1.0-alpha.1](https://github.com/srikar298c/neon/compare/v0.0.1-alpha.0...v0.1.0-alpha.1)

### ⚠ BREAKING CHANGES

* always use async walredo, warn if sync is configured ([#7754](https://github.com/srikar298c/neon/issues/7754))
* use larger buffers for blob_io and ephemeral_file ([#7485](https://github.com/srikar298c/neon/issues/7485))

### Features

* allow detaching from ancestor for timelines without writes ([#7639](https://github.com/srikar298c/neon/issues/7639)) ([6351313](https://github.com/srikar298c/neon/commit/6351313ae96ab6d0e3e2b27ed2d86eed3dd004c9)), closes [#6994](https://github.com/srikar298c/neon/issues/6994)
* **pagebench:** add aux file bench ([#7746](https://github.com/srikar298c/neon/issues/7746)) ([e1a9669](https://github.com/srikar298c/neon/commit/e1a9669d05374ea27685a1cf527676fe01df7722))
* **pageserver:** add aux-file-v2 flag on tenant level ([#7505](https://github.com/srikar298c/neon/issues/7505)) ([dbe0aa6](https://github.com/srikar298c/neon/commit/dbe0aa653ac2d0c3ef0a8087b7ab8878d1e59c9a))
* **pageserver:** add metrics for aux file size ([#7623](https://github.com/srikar298c/neon/issues/7623)) ([7f51764](https://github.com/srikar298c/neon/commit/7f517640011a5dc2c811c66c2767ae58e27d0c79))
* **pageserver:** add scan interface ([#7468](https://github.com/srikar298c/neon/issues/7468)) ([a3fe12b](https://github.com/srikar298c/neon/commit/a3fe12b6d898205bddae4f06947841e14c98ff8e))
* **pageserver:** auto-detect previous aux file policy ([#7841](https://github.com/srikar298c/neon/issues/7841)) ([64577cf](https://github.com/srikar298c/neon/commit/64577cfddcdac89d649e1ba6db3a6f44e14e2eee))
* **pageserver:** do not read past image layers for vectored get ([#7773](https://github.com/srikar298c/neon/issues/7773)) ([6810d2a](https://github.com/srikar298c/neon/commit/6810d2aa53b7b7646013d2f236d155a4f1b4721d))
* **pageserver:** generate basebackup from aux file v2 storage ([#7517](https://github.com/srikar298c/neon/issues/7517)) ([017c34b](https://github.com/srikar298c/neon/commit/017c34b7736119f250c68c8f2aecfdee2866dc5f))
* **pageserver:** generate image layers for sparse keyspace ([#7567](https://github.com/srikar298c/neon/issues/7567)) ([7701ca4](https://github.com/srikar298c/neon/commit/7701ca45dd2215ecca8b8c3de50926ae9b520ffd))
* **pageserver:** persist aux file policy in index part ([#7668](https://github.com/srikar298c/neon/issues/7668)) ([aaf6081](https://github.com/srikar298c/neon/commit/aaf60819fa479e37a4b477b20e1fbcee2d5a046f))
* **pageserver:** separate sparse and dense keyspace  ([#7503](https://github.com/srikar298c/neon/issues/7503)) ([45c625f](https://github.com/srikar298c/neon/commit/45c625fb349c3dbe711e5868bfa389da298bc960))
* **pageserver:** use fnv hash for aux file encoding ([#7742](https://github.com/srikar298c/neon/issues/7742)) ([4b97683](https://github.com/srikar298c/neon/commit/4b97683338bc21e13686fe4311946b36462729c1))
* Timeline detach ancestor ([#7456](https://github.com/srikar298c/neon/issues/7456)) ([3c9b484](https://github.com/srikar298c/neon/commit/3c9b484c4dbd52e286f17f3c6a5c6691990aa983)), closes [#6994](https://github.com/srikar298c/neon/issues/6994)


### Bug Fixes

* avoid starving background task permits in eviction task ([#7471](https://github.com/srikar298c/neon/issues/7471)) ([a60035b](https://github.com/srikar298c/neon/commit/a60035b23a2f05e512036131f5aef506e583c213))
* do not create metrics contention from background task permit ([#7730](https://github.com/srikar298c/neon/issues/7730)) ([4d8a10a](https://github.com/srikar298c/neon/commit/4d8a10af1cc41563cc4542beb327a2d75fb1bad8)), closes [#7161](https://github.com/srikar298c/neon/issues/7161)
* find gc cutoff points without holding Tenant::gc_cs ([#7585](https://github.com/srikar298c/neon/issues/7585)) ([ed9a114](https://github.com/srikar298c/neon/commit/ed9a114bde38b971f49dd12b53163587477fdcc4)), closes [#7560](https://github.com/srikar298c/neon/issues/7560) [#7587](https://github.com/srikar298c/neon/issues/7587)
* **Layer:** carry gate until eviction is complete ([#7838](https://github.com/srikar298c/neon/issues/7838)) ([62aac6c](https://github.com/srikar298c/neon/commit/62aac6c8add432da1ab2d206f19323e808622e8d))
* **metrics:** correct maxrss metrics on macos ([#7487](https://github.com/srikar298c/neon/issues/7487)) ([447a063](https://github.com/srikar298c/neon/commit/447a063f3c6583ed8e1946900493c1343b1daaef))
* **pageserver:** compile warning of download_object.ctx on macos ([#7596](https://github.com/srikar298c/neon/issues/7596)) ([3582a95](https://github.com/srikar298c/neon/commit/3582a95c8767fc39f037eed36e0fe3e1052443f2))
* **pageserver:** ensure to_i128 works for metadata keys ([#7895](https://github.com/srikar298c/neon/issues/7895)) ([1eca8b8](https://github.com/srikar298c/neon/commit/1eca8b8a6b56e82445d9d8354e7acfee97c80603))
* **pageserver:** make wal connstr a connstr ([#7846](https://github.com/srikar298c/neon/issues/7846)) ([e28e46f](https://github.com/srikar298c/neon/commit/e28e46f20be1f1bd298bbba6c5a131f435acde52))
* **pageserver:** properly propagate missing key error for vectored get ([#7569](https://github.com/srikar298c/neon/issues/7569)) ([f656db0](https://github.com/srikar298c/neon/commit/f656db09a4c0bc65fc249fd63c2d5c276f1860fa))
* **pageserver:** remove update_gc_info calls in tests ([#7608](https://github.com/srikar298c/neon/issues/7608)) ([ef03b38](https://github.com/srikar298c/neon/commit/ef03b38e5282140a5b7003c7f5010e1707631f31))
* **test suite:** forward compat test is not using latest neon_local ([#7637](https://github.com/srikar298c/neon/issues/7637)) ([ea531d4](https://github.com/srikar298c/neon/commit/ea531d448eb65c4f58abb9ef7d8cd461952f7c5f))
* **test:** ensure compatibility test uses the correct compute node ([#7741](https://github.com/srikar298c/neon/issues/7741)) ([9ffb852](https://github.com/srikar298c/neon/commit/9ffb8523597d846b6afce7eb855b820b79efcbd6))
* **test:** ensure fixtures are correctly used for pageserver_aux_file_policy ([#7769](https://github.com/srikar298c/neon/issues/7769)) ([c6d5ff9](https://github.com/srikar298c/neon/commit/c6d5ff944db91f498e46fa24eb0d667abdf94dba))
* **test:** update the config for neon_binpath in from_repo_dir ([#7684](https://github.com/srikar298c/neon/issues/7684)) ([b9fd8dc](https://github.com/srikar298c/neon/commit/b9fd8dcf13e13b804047fc21089d2ecb509a1548))
* **virtual_file:** compile warnings on macos ([#7525](https://github.com/srikar298c/neon/issues/7525)) ([75b4440](https://github.com/srikar298c/neon/commit/75b4440d0786b4f53c5ca26e9c7ed8b88bc4b40b))


### Performance Improvements

* **pageserver:** postpone vectored get fringe keyspace construction ([#7904](https://github.com/srikar298c/neon/issues/7904)) ([33395dc](https://github.com/srikar298c/neon/commit/33395dcf4ef137b39d3ba8022e9e4d07e7de9ed4))
* use larger buffers for blob_io and ephemeral_file ([#7485](https://github.com/srikar298c/neon/issues/7485)) ([ed57772](https://github.com/srikar298c/neon/commit/ed577727936b18479a6d04c2449bb77eb8245e19))


### Chores

* always use async walredo, warn if sync is configured ([#7754](https://github.com/srikar298c/neon/issues/7754)) ([c3dd646](https://github.com/srikar298c/neon/commit/c3dd646ab3a48e1063c7efc6d080e21fdfb48fa7))
* **deps:** use upstream svg_fmt after they merged our PR ([#7764](https://github.com/srikar298c/neon/issues/7764)) ([bc78b0e](https://github.com/srikar298c/neon/commit/bc78b0e9cc95ea033797b13d5bb36e61d338a070))
* go live ([#1](https://github.com/srikar298c/neon/issues/1)) ([49de7a5](https://github.com/srikar298c/neon/commit/49de7a5047b2a5a25c4c7b8b8eb30732a16d0511))
* lower gate guard drop logging threshold to 100ms ([#7862](https://github.com/srikar298c/neon/issues/7862)) ([a3f5b83](https://github.com/srikar298c/neon/commit/a3f5b836772d54464e18302beb132f4c19b8adf8))
* **neon_test_utils:** restrict installation to superuser ([#7624](https://github.com/srikar298c/neon/issues/7624)) ([1173ee6](https://github.com/srikar298c/neon/commit/1173ee6a7e1168e671a6847eb94807b45c703490))
* **pageserver:** add force aux file policy switch handler ([#7842](https://github.com/srikar298c/neon/issues/7842)) ([4a278cc](https://github.com/srikar298c/neon/commit/4a278cce7ce5b7f32360e85fd41219df95cc9a86))
* **pageserver:** categorize basebackup errors ([#7523](https://github.com/srikar298c/neon/issues/7523)) ([5558457](https://github.com/srikar298c/neon/commit/5558457c84c2cb2c948989a2ac4139322dce50e3))
* **pageserver:** concise error message for layer traversal ([#7565](https://github.com/srikar298c/neon/issues/7565)) ([26e6ff8](https://github.com/srikar298c/neon/commit/26e6ff8ba61c896cae9fd35c1683b0126203f345))
* **pageserver:** improve in-memory layer vectored get ([#7467](https://github.com/srikar298c/neon/issues/7467)) ([11945e6](https://github.com/srikar298c/neon/commit/11945e64ecec437caf5840edfa7a31ac765ce5e1))
* **pageserver:** plumb through RequestContext to VirtualFile open methods ([#7725](https://github.com/srikar298c/neon/issues/7725)) ([6ff7429](https://github.com/srikar298c/neon/commit/6ff74295b5b21d54192d20d114d78621d8d53ba0))
* **pageserver:** plumb through RequestContext to VirtualFile read methods ([#7720](https://github.com/srikar298c/neon/issues/7720)) ([b58a615](https://github.com/srikar298c/neon/commit/b58a615197374da349525da843b04849c47d610f))
* **pageserver:** plumb through RequestContext to VirtualFile write methods ([#7566](https://github.com/srikar298c/neon/issues/7566)) ([45ec868](https://github.com/srikar298c/neon/commit/45ec8688ea27cbad9789aac934a23069cbe95595))
* **pageserver:** reduce logging related to image layers ([#7864](https://github.com/srikar298c/neon/issues/7864)) ([6b31642](https://github.com/srikar298c/neon/commit/6b3164269cc3a6c577428071986447aadffc0008))
* **pageserver:** remove metrics for in-memory ingestion ([#7823](https://github.com/srikar298c/neon/issues/7823)) ([e3f6a07](https://github.com/srikar298c/neon/commit/e3f6a07ca300549181042752c5943c71424e476a))
* **pageserver:** shrink aux keyspace to 0x60-0x7F ([#7502](https://github.com/srikar298c/neon/issues/7502)) ([ee3437c](https://github.com/srikar298c/neon/commit/ee3437cbd8d539d00cc0789b7314d8a995668a9d))
* **pageserver:** temporary metrics on ingestion time ([#7515](https://github.com/srikar298c/neon/issues/7515)) ([c59abed](https://github.com/srikar298c/neon/commit/c59abedd85b81d832225a2490ba066e0c6993fc9))
* **pageserver:** use kebab case for aux file flag ([#7840](https://github.com/srikar298c/neon/issues/7840)) ([ddd8ebd](https://github.com/srikar298c/neon/commit/ddd8ebd2536f90872da2678aecbd94a3e1b3f547))
* **pageserver:** use kebab case for compaction algorithms ([#7845](https://github.com/srikar298c/neon/issues/7845)) ([ff560a1](https://github.com/srikar298c/neon/commit/ff560a1113046ff29acf2723c0183db7c2d128f1))
* **pageserver:** warn on delete non-existing file ([#7847](https://github.com/srikar298c/neon/issues/7847)) ([f20a9e7](https://github.com/srikar298c/neon/commit/f20a9e760fc7371c84c550adcb3fe6c553610c96))
* sync repo ([9090609](https://github.com/srikar298c/neon/commit/9090609c93851fbe091c769d906c269c34a1b290))
* **test:** add version check for forward compat test ([#7685](https://github.com/srikar298c/neon/issues/7685)) ([30d15ad](https://github.com/srikar298c/neon/commit/30d15ad4032e543be37fc0378345d9b6568b20cc))
* update defaults for timeline_detach_ancestor ([#7779](https://github.com/srikar298c/neon/issues/7779)) ([c1390bf](https://github.com/srikar298c/neon/commit/c1390bfc3bbd3a7f00df334a39220ca312fc888e))
* **vm-image:** specify sql exporter listen port ([#7526](https://github.com/srikar298c/neon/issues/7526)) ([89cae64](https://github.com/srikar298c/neon/commit/89cae64e38a68045b1f748d5b15d5cd607c9958a))


### Documentation

* fix unintentional file link ([#7506](https://github.com/srikar298c/neon/issues/7506)) ([84b6b95](https://github.com/srikar298c/neon/commit/84b6b95783eaecea06b40e2e87ddcdd70aa9e504))


### Refactors

* **ephemeral_file:** reuse owned_buffers_io::BufferedWriter ([#7484](https://github.com/srikar298c/neon/issues/7484)) ([dbb0c96](https://github.com/srikar298c/neon/commit/dbb0c967d5fb5104847fb71e8d783ebeae3e7ff2))
* move `NodeMetadata` to `pageserver_api`; use it from `neon_local` ([#7606](https://github.com/srikar298c/neon/issues/7606)) ([1e7cd6a](https://github.com/srikar298c/neon/commit/1e7cd6ac9f3568ffe9db952cb89f8036330d27b5))
* **owned_buffer_io::util::size_tracking_writer:** make generic over underlying writer ([#7483](https://github.com/srikar298c/neon/issues/7483)) ([bf369f4](https://github.com/srikar298c/neon/commit/bf369f4268f839b5228dd1d65d822280d50401c8))
* **owned_buffers_io::BufferedWriter:** be generic over the type of buffer ([#7482](https://github.com/srikar298c/neon/issues/7482)) ([70f4a16](https://github.com/srikar298c/neon/commit/70f4a16a05a5512c250102600f7900169b15c56d))
* **pageserver:** remove --update-init flag ([#7612](https://github.com/srikar298c/neon/issues/7612)) ([df1def7](https://github.com/srikar298c/neon/commit/df1def70183f0deb416e68b427e933724c950f9e))
* **rtc:** remove excess cloning ([#7635](https://github.com/srikar298c/neon/issues/7635)) ([d041f9a](https://github.com/srikar298c/neon/commit/d041f9a8872771a94075215605f624e861e081a8))
* **rtc:** remove the duplicate IndexLayerMetadata ([#7860](https://github.com/srikar298c/neon/issues/7860)) ([7cf726e](https://github.com/srikar298c/neon/commit/7cf726e36e3a9dab2516a861b914eda3d2cac2c4))
* **test:** duplication with fullbackup, tar content hashing ([#7828](https://github.com/srikar298c/neon/issues/7828)) ([df9ab1b](https://github.com/srikar298c/neon/commit/df9ab1b5e3962da4d98c7b1cd6a7fa20f4ff3902)), closes [#7715](https://github.com/srikar298c/neon/issues/7715)
* **update_gc_info:** split GcInfo to compose out of GcCutoffs ([#7584](https://github.com/srikar298c/neon/issues/7584)) ([60f570c](https://github.com/srikar298c/neon/commit/60f570c70da0fec651b5fd5de0d551b60d5f53b6)), closes [#7560](https://github.com/srikar298c/neon/issues/7560)


### Build System

* **deps:** bump flask-cors from 3.0.10 to 4.0.1 ([#7633](https://github.com/srikar298c/neon/issues/7633)) ([2dbd1c1](https://github.com/srikar298c/neon/commit/2dbd1c1ed5cd0458933e8ffd40a9c0a5f4d610b8))
* **deps:** bump jinja2 from 3.1.3 to 3.1.4 ([#7626](https://github.com/srikar298c/neon/issues/7626)) ([5a3d8e7](https://github.com/srikar298c/neon/commit/5a3d8e75edd5f684726b662638c833f02b1423e6))
* **deps:** bump moto from 4.1.2 to 5.0.6 ([#7653](https://github.com/srikar298c/neon/issues/7653)) ([a4a4d78](https://github.com/srikar298c/neon/commit/a4a4d78993781e7aa723c1df6b833435c2fb2e8c))
* **deps:** bump Npgsql from 8.0.2 to 8.0.3 in /test_runner/pg_clients/csharp/npgsql ([#7680](https://github.com/srikar298c/neon/issues/7680)) ([5ea117c](https://github.com/srikar298c/neon/commit/5ea117cddfe3bc58c500f0eff8352af796b58268))
* **deps:** bump requests from 2.31.0 to 2.32.0 ([#7816](https://github.com/srikar298c/neon/issues/7816)) ([baeb584](https://github.com/srikar298c/neon/commit/baeb58432f77809f68eb648481e81ed5af15a8b0))
* **deps:** bump werkzeug from 3.0.1 to 3.0.3 ([#7625](https://github.com/srikar298c/neon/issues/7625)) ([6e4e578](https://github.com/srikar298c/neon/commit/6e4e578841ce9ec09a8b8e255a511163407901bd))
* run doctests ([#7697](https://github.com/srikar298c/neon/issues/7697)) ([6206f76](https://github.com/srikar298c/neon/commit/6206f76419416c6c936c97df5e660d28333ee835))
