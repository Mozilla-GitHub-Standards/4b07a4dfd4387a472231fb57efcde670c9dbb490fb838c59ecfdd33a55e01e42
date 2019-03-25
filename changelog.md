##  Commits in production - for 3 days, generated on: 2019-03-25 18:51:56 UTC.
|	autoland	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/autoland.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/autoland.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=9e8fee5e4f3d)|[Bug 1519825 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1519825) - Update grcov to revision 9214a916805838265764f9c69eaed657ea3db021 r=marco This revision corresponds to grcov 0.4.2 Differential Revision: https://phabricator.services.mozilla.com/D16465|csabou@mozilla.com|marco|2019-03-25 19:17:14|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=775f40c959fc)|[Bug 1538134 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538134) [mozharness] Set repository path in taskcluster; r=aki Taskcluster has authorative information about the repository being built, so pass that to mozharness, rather than have mozharness reconstruct it from hand-maintained mozharness config. Differential Revision: https://phabricator.services.mozilla.com/D24561|mozilla@hocat.ca|aki|2019-03-25 18:06:32|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=db11228c8a38)|[Bug 1538134 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538134) [mozharness] Remove explicit setting of branches to use release promotion; r=aki The only thing this affects is the default update channel, but for shipping builds, this is set explicitly via taskcluster, and for other branches, defaults to `default`. Differential Revision: https://phabricator.services.mozilla.com/D24562|mozilla@hocat.ca|aki|2019-03-25 18:06:32|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=3e4b58569126)|[Bug 1538134 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538134) [mozharness] Don't override PGO settings per-branch; r=aki The release mozconfigs set `MOZ_PGO` and all shipping builds set the `nightly` mozharness config, so we don't need to additionaly set PGO based on the branch. Differential Revision: https://phabricator.services.mozilla.com/D24563|mozilla@hocat.ca|aki|2019-03-25 18:06:32|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=d5c2b9a1c215)|[Bug 1538134 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538134) [mozharness] Remove support for unused `builds/branch_specifics.py` config; r=aki We have moved per-branch configuration to taskcluster, so we can remove that support in mozharness. Differential Revision: https://phabricator.services.mozilla.com/D24564|mozilla@hocat.ca|aki|2019-03-25 18:06:32|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=02b78c6e3ca7)|[Bug 1536839 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536839) - Add json formatter to ./mach clang-format, r=ahal,marco Depends on D24193 Differential Revision: https://phabricator.services.mozilla.com/D24194|babadie@mozilla.com|ahal,marco|2019-03-25 17:04:23|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=486437866d00)|[Bug 1535679 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1535679) - switch Firefox nightlies to declarative artifacts. r=sfraser a=release Linter fixes. Differential Revision: https://phabricator.services.mozilla.com/D24214|mtabara@mozilla.com|sfraser|2019-03-25 15:50:16|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=5a3f8b7e664c)|No Bug, taskcluster/docker/funsize-update-generator pipfile-update. r=sfraser Differential Revision: https://phabricator.services.mozilla.com/D24676|sfraser@mozilla.com|sfraser|2019-03-25 13:08:53|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=4d546ab0dc94)|[Bug 1538475 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538475) - Add comma to 'central-to-beta' and 'beta-to-release' generators to prevent concatenation of two folder paths of files to modify r=jlorenzo Differential Revision: https://phabricator.services.mozilla.com/D24602|archaeopteryx@coole-files.de|jlorenzo|2019-03-25 11:25:37|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=43ac43ba6cf4)|[Bug 1536836 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536836) - Support multiple formatters with file output in ./mach lint, r=ahal Differential Revision: https://phabricator.services.mozilla.com/D24193|babadie@mozilla.com|ahal|2019-03-25 11:17:44|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=4983a9d119c7)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Enable EME on win64-aarch64 nightlies. r=tomprince [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) added win64-aarch64-eme/opt builds, which are artifact builds that glue together a win64-aarch64/opt build and a win32/opt build. This enables EME on the corresponding nightlies in a slightly different way: - this adds a no-eme build that corresponds to win64-aarch64/opt. - this turns the existing nightly into an artifact build that glues together that no-eme build and the win32 nightly. The no-eme build cannot have the nightly attribute set, first because the beetmover transform fails in that case, and because that would imply shipping those builds, but they're not meant to be shipped this way. It also has run-on-projects set to an empty list so that it doesn't appear by default in `mach try fuzzy`, while still being triggered when needed due to being a dependency of the nightly build. It is preferable to keep the win64-aarch64{,-eme}/opt builds untouched to make things easier for try (the win64-aarch64 ones being the main ones to try; also, the -eme builds currently fail with --artifacts). Ideally, like in [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) we'd add a diffoscope build to ensure the variations between the nightly and its base no-eme build are within control, but currently, that would trigger nightlies on every push, which is not desirable. Ideally, they'd trigger whenever both their dependencies are in the target task graph. We leave that to a followup. Differential Revision: https://phabricator.services.mozilla.com/D23640|shindli@mozilla.com|tomprince|2019-03-23 11:51:09|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=e1e990731d52)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Apply same changes as win64-aarch64 nightlies to the shippable builds. r=tomprince Differential Revision: https://phabricator.services.mozilla.com/D24573|shindli@mozilla.com|tomprince|2019-03-23 11:51:09|

|	mozilla-inbound	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-inbound.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-inbound.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=43ac43ba6cf4)|[Bug 1536836 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536836) - Support multiple formatters with file output in ./mach lint, r=ahal Differential Revision: https://phabricator.services.mozilla.com/D24193|aiakab@mozilla.com|ahal|2019-03-25 17:58:26|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=4d546ab0dc94)|[Bug 1538475 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538475) - Add comma to 'central-to-beta' and 'beta-to-release' generators to prevent concatenation of two folder paths of files to modify r=jlorenzo Differential Revision: https://phabricator.services.mozilla.com/D24602|aiakab@mozilla.com|jlorenzo|2019-03-25 17:58:26|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=5a3f8b7e664c)|No Bug, taskcluster/docker/funsize-update-generator pipfile-update. r=sfraser Differential Revision: https://phabricator.services.mozilla.com/D24676|aiakab@mozilla.com|sfraser|2019-03-25 17:58:26|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=b95fc834fb68)|[Bug 1538198 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538198) - Trigger a bugzilla-components job along with the searchfox indexing jobs. r=emilio Searchfox relies on the bugzilla component job running on the same push as the indexing jobs, but there's nothing that actually guarantees that. Thus far pushes to m-c pretty much always have source changes so the bugzilla component job gets run, but on beta/release branches it's possible to get pushes with just tag changes and no source changes, so the bugzilla component job would get optimized away. This patch ensures that the job gets run along with the other indexing jobs that searchfox needs. Differential Revision: https://phabricator.services.mozilla.com/D24507|shindli@mozilla.com|emilio|2019-03-23 11:54:29|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=5643338d4df0)|No bug: [diffoscope] Output an empty diff if the files do not differ; r=glandium Currently, if the files match and you try to look at the diff, you get { "reason": "file-missing-on-worker", "message": "Artifact \"public/diff.html\" not found at \"/builds/worker/diff.html\"" } which makes it hard to tell if there was an error generating a diff, or if the files matched. This changes things to ask diffoscope to always output a diff, to remedy that confusion. Differential Revision: https://phabricator.services.mozilla.com/D24316|shindli@mozilla.com|glandium|2019-03-23 11:54:29|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=403eb141fe90)|[Bug 1536882 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536882) Stop specifying installer to download in windows L10n jobs; r=Callek The code that actually downloads it is behind a condition that isn't set anywhere. Differential Revision: https://phabricator.services.mozilla.com/D24215|shindli@mozilla.com|Callek|2019-03-23 11:54:29|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=5d251a7e6031)|[Bug 1536103 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536103) - Fix Sphinx Warning - Title Underline too short in 'mach doc'. r=ahal Differential Revision: https://phabricator.services.mozilla.com/D24536|shindli@mozilla.com|ahal|2019-03-23 11:54:29|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=4983a9d119c7)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Enable EME on win64-aarch64 nightlies. r=tomprince [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) added win64-aarch64-eme/opt builds, which are artifact builds that glue together a win64-aarch64/opt build and a win32/opt build. This enables EME on the corresponding nightlies in a slightly different way: - this adds a no-eme build that corresponds to win64-aarch64/opt. - this turns the existing nightly into an artifact build that glues together that no-eme build and the win32 nightly. The no-eme build cannot have the nightly attribute set, first because the beetmover transform fails in that case, and because that would imply shipping those builds, but they're not meant to be shipped this way. It also has run-on-projects set to an empty list so that it doesn't appear by default in `mach try fuzzy`, while still being triggered when needed due to being a dependency of the nightly build. It is preferable to keep the win64-aarch64{,-eme}/opt builds untouched to make things easier for try (the win64-aarch64 ones being the main ones to try; also, the -eme builds currently fail with --artifacts). Ideally, like in [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) we'd add a diffoscope build to ensure the variations between the nightly and its base no-eme build are within control, but currently, that would trigger nightlies on every push, which is not desirable. Ideally, they'd trigger whenever both their dependencies are in the target task graph. We leave that to a followup. Differential Revision: https://phabricator.services.mozilla.com/D23640|mh@glandium.org|tomprince|2019-03-23 02:30:00|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=e1e990731d52)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Apply same changes as win64-aarch64 nightlies to the shippable builds. r=tomprince Differential Revision: https://phabricator.services.mozilla.com/D24573|mh@glandium.org|tomprince|2019-03-23 02:30:00|

|	mozilla-central	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-central.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-central.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=43ac43ba6cf4)|[Bug 1536836 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536836) - Support multiple formatters with file output in ./mach lint, r=ahal Differential Revision: https://phabricator.services.mozilla.com/D24193|aiakab@mozilla.com|ahal|2019-03-25 17:52:30|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=4d546ab0dc94)|[Bug 1538475 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538475) - Add comma to 'central-to-beta' and 'beta-to-release' generators to prevent concatenation of two folder paths of files to modify r=jlorenzo Differential Revision: https://phabricator.services.mozilla.com/D24602|aiakab@mozilla.com|jlorenzo|2019-03-25 17:52:30|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=5a3f8b7e664c)|No Bug, taskcluster/docker/funsize-update-generator pipfile-update. r=sfraser Differential Revision: https://phabricator.services.mozilla.com/D24676|aiakab@mozilla.com|sfraser|2019-03-25 17:52:30|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=4983a9d119c7)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Enable EME on win64-aarch64 nightlies. r=tomprince [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) added win64-aarch64-eme/opt builds, which are artifact builds that glue together a win64-aarch64/opt build and a win32/opt build. This enables EME on the corresponding nightlies in a slightly different way: - this adds a no-eme build that corresponds to win64-aarch64/opt. - this turns the existing nightly into an artifact build that glues together that no-eme build and the win32 nightly. The no-eme build cannot have the nightly attribute set, first because the beetmover transform fails in that case, and because that would imply shipping those builds, but they're not meant to be shipped this way. It also has run-on-projects set to an empty list so that it doesn't appear by default in `mach try fuzzy`, while still being triggered when needed due to being a dependency of the nightly build. It is preferable to keep the win64-aarch64{,-eme}/opt builds untouched to make things easier for try (the win64-aarch64 ones being the main ones to try; also, the -eme builds currently fail with --artifacts). Ideally, like in [Bug 1534522 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1534522) we'd add a diffoscope build to ensure the variations between the nightly and its base no-eme build are within control, but currently, that would trigger nightlies on every push, which is not desirable. Ideally, they'd trigger whenever both their dependencies are in the target task graph. We leave that to a followup. Differential Revision: https://phabricator.services.mozilla.com/D23640|shindli@mozilla.com|tomprince|2019-03-23 11:48:05|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=e1e990731d52)|[Bug 1527463 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1527463) - Apply same changes as win64-aarch64 nightlies to the shippable builds. r=tomprince Differential Revision: https://phabricator.services.mozilla.com/D24573|shindli@mozilla.com|tomprince|2019-03-23 11:48:05|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=b95fc834fb68)|[Bug 1538198 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538198) - Trigger a bugzilla-components job along with the searchfox indexing jobs. r=emilio Searchfox relies on the bugzilla component job running on the same push as the indexing jobs, but there's nothing that actually guarantees that. Thus far pushes to m-c pretty much always have source changes so the bugzilla component job gets run, but on beta/release branches it's possible to get pushes with just tag changes and no source changes, so the bugzilla component job would get optimized away. This patch ensures that the job gets run along with the other indexing jobs that searchfox needs. Differential Revision: https://phabricator.services.mozilla.com/D24507|shindli@mozilla.com|emilio|2019-03-23 11:46:24|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=5643338d4df0)|No bug: [diffoscope] Output an empty diff if the files do not differ; r=glandium Currently, if the files match and you try to look at the diff, you get { "reason": "file-missing-on-worker", "message": "Artifact \"public/diff.html\" not found at \"/builds/worker/diff.html\"" } which makes it hard to tell if there was an error generating a diff, or if the files matched. This changes things to ask diffoscope to always output a diff, to remedy that confusion. Differential Revision: https://phabricator.services.mozilla.com/D24316|shindli@mozilla.com|glandium|2019-03-23 11:46:24|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=403eb141fe90)|[Bug 1536882 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536882) Stop specifying installer to download in windows L10n jobs; r=Callek The code that actually downloads it is behind a condition that isn't set anywhere. Differential Revision: https://phabricator.services.mozilla.com/D24215|shindli@mozilla.com|Callek|2019-03-23 11:46:24|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=5d251a7e6031)|[Bug 1536103 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1536103) - Fix Sphinx Warning - Title Underline too short in 'mach doc'. r=ahal Differential Revision: https://phabricator.services.mozilla.com/D24536|shindli@mozilla.com|ahal|2019-03-23 11:46:24|

|	mozilla-beta	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-beta.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-beta.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/releases/mozilla-beta/pushloghtml?changeset=de506694d256)|[Bug 1538198 ](https://bugzilla.mozilla.org/show_bug.cgi?id=1538198) - Trigger a bugzilla-components job along with the searchfox indexing jobs. r=emilio a=searchfox-only Searchfox relies on the bugzilla component job running on the same push as the indexing jobs, but there's nothing that actually guarantees that. Thus far pushes to m-c pretty much always have source changes so the bugzilla component job gets run, but on beta/release branches it's possible to get pushes with just tag changes and no source changes, so the bugzilla component job would get optimized away. This patch ensures that the job gets run along with the other indexing jobs that searchfox needs. Differential Revision: https://phabricator.services.mozilla.com/D24507|kgupta@mozilla.com|emilio|2019-03-23 16:39:31|

|	mozilla-release	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-release.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-release.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-release.md)|FIC - BOT|Self Generated| - |

|	build-puppet	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.md)|FIC - BOT|Self Generated| - |

|	OpenCloudConfig	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.md)|FIC - BOT|Self Generated| - |

|	taskcluster	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/taskcluster.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/taskcluster.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://github.com/taskcluster/taskcluster/commit/b3c5082752df072263c7da1d7b53a8fe0a8fbefe)|Merge pull request #481 from taskcluster/issue-479  Cleanup logs docs pages|imbstack|N/A|2019-03-25 18:47:11|
|[Link](https://github.com/taskcluster/taskcluster/commit/bed82c7c4881fab007eecb8bf1cfe1c6033810f5)|Show access token when creating a client (#489)|helfi92|N/A|2019-03-25 17:26:24|
|[Link](https://github.com/taskcluster/taskcluster/commit/02020bdea61450b4c3ec0cc0c21c507f7f0ab9e9)|Merge pull request #491 from taskcluster/renovate/raw-loader-2.x  Update dependency raw-loader to v2|djmitche|N/A|2019-03-25 13:51:44|
|[Link](https://github.com/taskcluster/taskcluster/commit/3cea3dd67620033912d99c9500a43d3af02d321c)|Merge pull request #463 from helfi92/nicer-getting-started-page  [UI] Add custom get started view|helfi92|N/A|2019-03-25 13:37:18|
|[Link](https://github.com/taskcluster/taskcluster/commit/aed11bbf3b0eba07caba51db539027090ce42ce0)|Update dependency raw-loader to v2|renovate-bot|N/A|2019-03-25 13:34:31|
|[Link](https://github.com/taskcluster/taskcluster/commit/182d385465c2abe482b18fcb15033715af7f3a88)|Merge pull request #493 from taskcluster/renovate/serialize-error-4.x  Update dependency serialize-error to v4|djmitche|N/A|2019-03-25 13:20:07|
|[Link](https://github.com/taskcluster/taskcluster/commit/6cc9ec0839d506243b5651a329d356abe8254db8)|Update dependency serialize-error to v4|renovate-bot|N/A|2019-03-25 13:05:42|
|[Link](https://github.com/taskcluster/taskcluster/commit/d6d64d9ee9ea0e2fb7793a69259922b112067089)|Merge pull request #490 from taskcluster/renovate/eslint-5.x  Update dependency eslint to v5.15.3|djmitche|N/A|2019-03-25 13:04:33|
|[Link](https://github.com/taskcluster/taskcluster/commit/fa15721bb6f1b9c0d91a20f72ce78ebcbe11aa31)|Adjust GetStarted url in markdown|helfi92|N/A|2019-03-25 12:47:37|
|[Link](https://github.com/taskcluster/taskcluster/commit/3d8177c3c34f2d9111059310d4f83dd676d39dc8)|Linting|helfi92|N/A|2019-03-23 17:41:00|
|[Link](https://github.com/taskcluster/taskcluster/commit/91e836d45b624a5e46045d0fc93ad6dbd5a3a9b1)|Add section for the people behind taskcluster in docs|helfi92|N/A|2019-03-23 17:40:18|
|[Link](https://github.com/taskcluster/taskcluster/commit/bce0d8df52fcc4c6b273a8ba644dcca3185a689b)|Make card clickable instead of "See more" button|helfi92|N/A|2019-03-23 17:30:03|
|[Link](https://github.com/taskcluster/taskcluster/commit/a809600db384a67c6d7a18311d773cd0868dfe09)|Merge pull request #483 from djmitche/docs-error-handling  Simplify docs loading and improve error handling|djmitche|N/A|2019-03-23 22:46:38|
|[Link](https://github.com/taskcluster/taskcluster/commit/b09829e03804399c6cd6b6517e3d1e35aebcac4c)|remove debugging output|djmitche|N/A|2019-03-22 23:11:57|
|[Link](https://github.com/taskcluster/taskcluster/commit/daacd3df17480a7ce07f3cce19a9f5ddd991bed4)|Merge pull request #487 from djmitche/bug1533937-b  Bug 1533937 - cleanup after tests (azure tables, at least) on push|djmitche|N/A|2019-03-22 23:08:47|
|[Link](https://github.com/taskcluster/taskcluster/commit/375b1ff343479bb9b284f04dc4514ee54fd8879b)|Bug 1533937 - cleanup after tests (azure tables, at least) on push|djmitche|N/A|2019-03-22 22:23:17|
|[Link](https://github.com/taskcluster/taskcluster/commit/ce65ab0014077bef4e5336a98b53c52a2b223ad8)|Merge pull request #486 from djmitche/issue472  Replace dead link to presentations to a link to the youtube group|djmitche|N/A|2019-03-22 20:58:26|
|[Link](https://github.com/taskcluster/taskcluster/commit/b6a6c37d234ceb212ef8337e3bb1a84240de6adf)|Merge pull request #485 from djmitche/issue448  Drop unused reference categories|djmitche|N/A|2019-03-22 20:58:17|
|[Link](https://github.com/taskcluster/taskcluster/commit/ae7133cf0588abde66e3d5d4422f67386b53b82d)|Merge pull request #484 from taskcluster/all-contributors/add-sudipt1999  docs: add sudipt1999 as a contributor|djmitche|N/A|2019-03-22 20:45:57|
|[Link](https://github.com/taskcluster/taskcluster/commit/08bc4a4c28c8b891a668860eaf5cad682f5567dd)|Replace dead link to presentations to a link to the youtube group  This also drops the Travis-CI link.  We don't use Travis-CI for much anymore.|djmitche|N/A|2019-03-22 20:43:55|
|[Link](https://github.com/taskcluster/taskcluster/commit/79753bfff994add79faf8503ee7f13623f5853d7)|Drop unused reference categories  Fixes #448.|djmitche|N/A|2019-03-22 20:34:26|
|[Link](https://github.com/taskcluster/taskcluster/commit/9452002eb08c8e2d2924c861ec83d6238c100b4c)|docs: update .all-contributorsrc|allcontributors[bot]|N/A|2019-03-22 20:29:55|
|[Link](https://github.com/taskcluster/taskcluster/commit/bfa63f3df784b9d842c2cc76ffae57917418c36d)|docs: update README.md|allcontributors[bot]|N/A|2019-03-22 20:29:54|
|[Link](https://github.com/taskcluster/taskcluster/commit/b87579a5d844c75420eb734cbcc9dab31495d941)|Merge pull request #478 from taskcluster/bug-1537907  [Bug 1537907] Elide secret values|imbstack|N/A|2019-03-22 18:52:35|

|	addonscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.md)|FIC - BOT|Self Generated| - |

|	balrogscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.md)|FIC - BOT|Self Generated| - |

|	beetmoverscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.md)|FIC - BOT|Self Generated| - |

|	bouncerscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.md)|FIC - BOT|Self Generated| - |

|	pushapkscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.md)|FIC - BOT|Self Generated| - |

|	pushsnapscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.md)|FIC - BOT|Self Generated| - |

|	scriptworker	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.md)|FIC - BOT|Self Generated| - |

|	shipitscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.md)|FIC - BOT|Self Generated| - |

|	signingscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.md)|FIC - BOT|Self Generated| - |

|	signtool	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.md)|FIC - BOT|Self Generated| - |

|	treescript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.md)|FIC - BOT|Self Generated| - |

|	mozapkpublisher	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.md)|FIC - BOT|Self Generated| - |

|	services	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.md)|FIC - BOT|Self Generated| - |

|	build-cloud-tools	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.json)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.md)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.md)|FIC - BOT|Self Generated| - |

|	ci-configuration	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-configuration.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-configuration.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/ci/ci-configuration/pushloghtml?changeset=5a65955ea586)|No bug: Remove scopes associated to the deprecated taskcluster-worker; r=dustin Differential Revision: https://phabricator.services.mozilla.com/D24453|mozilla@hocat.ca|dustin|2019-03-22 23:59:05|
|[Link](https://hg.mozilla.org/ci/ci-configuration/pushloghtml?changeset=0dcbbd0b9cfe)|No bug: Remove scopes from branches that don't have jobs running on them; r=dustin Differential Revision: https://phabricator.services.mozilla.com/D24452|mozilla@hocat.ca|dustin|2019-03-22 23:44:57|

|	ci-admin	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-admin.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-admin.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last 3 days.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-admin.md)|FIC - BOT|Self Generated| - |
