##  Commits in production - for one day, generated on: 2019-02-25 22:41:45 UTC.
|	autoland	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/autoland.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/autoland.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=588497dfa9c0)|Bug 1530115 - Add nasm to searchfox builds. r=me |dluca@mozilla.com|me|2019-02-25 04:14:02|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=5727cf4eeb37)|Merge mozilla-inbound to mozilla-central. a=merge|dluca@mozilla.com|merge|2019-02-25 04:14:02|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=a238fb5cc415)|Backed out changeset e9e880f7aee4 (bug 1520163) for failing nightly builds a=backout|opoprus@mozilla.com|backout|2019-02-25 12:31:07|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=a5673a480930)|Backed out changeset 588497dfa9c0 (bug 1530115) as a dependency for Bug 1520163 a=backout|opoprus@mozilla.com|backout|2019-02-25 12:31:07|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=445315bbfbf9)|Backed out 10 changesets (bug 1521879) for causing bug 1530107. a=backout  Backed out changeset f597a73a6eac (bug 1521879) Backed out changeset 0bb76534f207 (bug 1521879) Backed out changeset abcb8be12adf (bug 1521879) Backed out changeset ed6c8d3bbfde (bug 1521879) Backed out changeset 1addf1e15b55 (bug 1521879) Backed out changeset 6b709cd9a479 (bug 1521879) Backed out changeset 07747027c59c (bug 1521879) Backed out changeset a6105ccc188c (bug 1521879) Backed out changeset 48c9c643e7bb (bug 1521879) Backed out changeset d4004105a04a (bug 1521879)|opoprus@mozilla.com|backout|2019-02-25 12:31:07|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=293617cdb29d)|Bug 1527777 - Move spidermonkey jobs from win32 to win64 r=jmaher  Differential Revision: https://phabricator.services.mozilla.com/D20619|sfink@mozilla.com|jmaher|2019-02-25 22:08:25|
|[Link](https://hg.mozilla.org/integration/autoland/pushloghtml?changeset=fae88bb4c6da)|Bug 1520163 - Add linux64-nasm toolchain. r=glandium  Differential Revision: https://phabricator.services.mozilla.com/D20037|tdaede@mozilla.com|glandium|2019-02-25 23:11:28|

|	ci-admin	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-admin.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-admin.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/ci/ci-admin/pushloghtml?changeset=933ac2604add)|No bug: Include `ci-admin check`'s `pytest.ini` in the installed package; r=dustin  Also stop using `--develop` (i.e. `-e`) when installing ci-admin in the check job. The addition of `pyproject.toml` triggers a pip bug[1], and we don't have a need to have an editable install.  [1] https://github.com/pypa/setuptools/issues/1405  Differential Revision: https://phabricator.services.mozilla.com/D20790|mozilla@hocat.ca|dustin|2019-02-25 18:49:25|

|	ci-configuration	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-configuration.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/ci-configuration.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/ci/ci-configuration/pushloghtml?changeset=a4184058abae)|Bug 1520867: Remove scopes for temporary bitbar worker; r=dustin  Differential Revision: https://phabricator.services.mozilla.com/D20788|mozilla@hocat.ca|dustin|2019-02-25 18:46:56|
|[Link](https://hg.mozilla.org/ci/ci-configuration/pushloghtml?changeset=18d5ea174bab)|Bug 1530376 - Update ci grants for code review task, r=dustin  Differential Revision: https://phabricator.services.mozilla.com/D21022|dmitchell@mozilla.com|dustin|2019-02-25 19:12:16|
|[Link](https://hg.mozilla.org/ci/ci-configuration/pushloghtml?changeset=ffbd916086f9)|Bug 1530170 - Grant 'queue:rerun-task:scheduler-id' as part of trust-domain-scopes; r=tomprince  Enables rerunning tasks from the taskcluster CLI client for Thunderbird developers.  Differential Revision: https://phabricator.services.mozilla.com/D21038|mozilla@hocat.ca|tomprince|2019-02-25 22:41:46|

|	mozilla-beta	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-beta.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-beta.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/releases/mozilla-beta/pushloghtml?changeset=17c78b631b58)|Bug 1529921: Use secrets from taskcluster for windows builds; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20849|mozilla@hocat.ca|aki|2019-02-25 07:17:05|
|[Link](https://hg.mozilla.org/releases/mozilla-beta/pushloghtml?changeset=f77b96743f3c)|Bug 1529921: [mozharness] Calculate scm_level for secrets directly from MOZ_SCM_LEVEL; r=aki a=tomprince  Differential Revision: https://phabricator.services.mozilla.com/D20893|mozilla@hocat.ca|aki|2019-02-25 07:17:05|

|	mozilla-central	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-central.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-central.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=dac57a397973)|Bug 1529921: Use secrets from taskcluster for windows builds; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20849|dluca@mozilla.com|aki|2019-02-25 03:46:40|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=94e616a3a7a0)|Bug 1529921: [mozharness] Calculate scm_level for secrets directly from MOZ_SCM_LEVEL; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20893|dluca@mozilla.com|aki|2019-02-25 03:46:40|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=588497dfa9c0)|Bug 1530115 - Add nasm to searchfox builds. r=me |dluca@mozilla.com|me|2019-02-25 03:48:16|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=5727cf4eeb37)|Merge mozilla-inbound to mozilla-central. a=merge|dluca@mozilla.com|merge|2019-02-25 03:48:16|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=a238fb5cc415)|Backed out changeset e9e880f7aee4 (bug 1520163) for failing nightly builds a=backout|aciure@mozilla.com|backout|2019-02-25 11:41:27|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=a5673a480930)|Backed out changeset 588497dfa9c0 (bug 1530115) as a dependency for Bug 1520163 a=backout|aciure@mozilla.com|backout|2019-02-25 11:55:32|
|[Link](https://hg.mozilla.org/mozilla-central/pushloghtml?changeset=445315bbfbf9)|Backed out 10 changesets (bug 1521879) for causing bug 1530107. a=backout  Backed out changeset f597a73a6eac (bug 1521879) Backed out changeset 0bb76534f207 (bug 1521879) Backed out changeset abcb8be12adf (bug 1521879) Backed out changeset ed6c8d3bbfde (bug 1521879) Backed out changeset 1addf1e15b55 (bug 1521879) Backed out changeset 6b709cd9a479 (bug 1521879) Backed out changeset 07747027c59c (bug 1521879) Backed out changeset a6105ccc188c (bug 1521879) Backed out changeset 48c9c643e7bb (bug 1521879) Backed out changeset d4004105a04a (bug 1521879)|rgurzau@mozilla.com|backout|2019-02-25 12:13:02|

|	mozilla-inbound	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-inbound.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-inbound.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=dac57a397973)|Bug 1529921: Use secrets from taskcluster for windows builds; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20849|dluca@mozilla.com|aki|2019-02-25 04:17:09|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=94e616a3a7a0)|Bug 1529921: [mozharness] Calculate scm_level for secrets directly from MOZ_SCM_LEVEL; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20893|dluca@mozilla.com|aki|2019-02-25 04:17:09|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=5727cf4eeb37)|Merge mozilla-inbound to mozilla-central. a=merge|dluca@mozilla.com|merge|2019-02-25 04:17:09|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=a238fb5cc415)|Backed out changeset e9e880f7aee4 (bug 1520163) for failing nightly builds a=backout|opoprus@mozilla.com|backout|2019-02-25 12:33:46|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=a5673a480930)|Backed out changeset 588497dfa9c0 (bug 1530115) as a dependency for Bug 1520163 a=backout|opoprus@mozilla.com|backout|2019-02-25 12:33:46|
|[Link](https://hg.mozilla.org/integration/mozilla-inbound/pushloghtml?changeset=445315bbfbf9)|Backed out 10 changesets (bug 1521879) for causing bug 1530107. a=backout  Backed out changeset f597a73a6eac (bug 1521879) Backed out changeset 0bb76534f207 (bug 1521879) Backed out changeset abcb8be12adf (bug 1521879) Backed out changeset ed6c8d3bbfde (bug 1521879) Backed out changeset 1addf1e15b55 (bug 1521879) Backed out changeset 6b709cd9a479 (bug 1521879) Backed out changeset 07747027c59c (bug 1521879) Backed out changeset a6105ccc188c (bug 1521879) Backed out changeset 48c9c643e7bb (bug 1521879) Backed out changeset d4004105a04a (bug 1521879)|opoprus@mozilla.com|backout|2019-02-25 12:33:46|

|	mozilla-release	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-release.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/hg_files/mozilla-release.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://hg.mozilla.org/releases/mozilla-release/pushloghtml?changeset=3feed900b297)|Bug 1529921: Use secrets from taskcluster for windows builds; r=aki  Differential Revision: https://phabricator.services.mozilla.com/D20849|mozilla@hocat.ca|aki|2019-02-25 07:18:16|
|[Link](https://hg.mozilla.org/releases/mozilla-release/pushloghtml?changeset=9f12c4ed7d9e)|Bug 1529921: [mozharness] Calculate scm_level for secrets directly from MOZ_SCM_LEVEL; r=aki a=tomprince  Differential Revision: https://phabricator.services.mozilla.com/D20893|mozilla@hocat.ca|aki|2019-02-25 07:18:16|

|	addonscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/addonscript.md)|FIC - BOT|Self Generated| - |

|	balrogscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/balrogscript.md)|FIC - BOT|Self Generated| - |

|	beetmoverscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/beetmoverscript.md)|FIC - BOT|Self Generated| - |

|	bouncerscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/bouncerscript.md)|FIC - BOT|Self Generated| - |

|	build-cloud-tools	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-cloud-tools.md)|FIC - BOT|Self Generated| - |

|	build-puppet	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/build-puppet.md)|FIC - BOT|Self Generated| - |

|	mozapkpublisher	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/mozapkpublisher.md)|FIC - BOT|Self Generated| - |

|	OpenCloudConfig	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/OpenCloudConfig.md)|FIC - BOT|Self Generated| - |

|	pushapkscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushapkscript.md)|FIC - BOT|Self Generated| - |

|	pushsnapscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/pushsnapscript.md)|FIC - BOT|Self Generated| - |

|	scriptworker	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/scriptworker.md)|FIC - BOT|Self Generated| - |

|	services	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/services.md)|FIC - BOT|Self Generated| - |

|	shipitscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/shipitscript.md)|FIC - BOT|Self Generated| - |

|	signingscript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signingscript.md)|FIC - BOT|Self Generated| - |

|	signtool	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/signtool.md)|FIC - BOT|Self Generated| - |

|	taskcluster	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/taskcluster.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/taskcluster.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
|[Link](https://github.com/taskcluster/taskcluster/commit/19479633df854a343f4f9b74cec13d0b2e035dc7)|Bug 1520579: Increase allowed length of worker-types in aws-provisoner UI (#303)|helfi92|N/A|2019-02-25 20:16:53|
|[Link](https://github.com/taskcluster/taskcluster/commit/7b058a76c4a92305c85083cfbcf19effcb53603a)|[UI] Add ability to prefetch components (hover/keyboard focus) (#278)    Add ability to prefetch components      Convert Link to a React Hook      Convert Links to use the new Link component|helfi92|N/A|2019-02-25 19:37:06|
|[Link](https://github.com/taskcluster/taskcluster/commit/fe161aea55d70d1ca7b76713507058db24de7485)|Merge pull request #292 from taskcluster/renovate/ajv-6.x  Update dependency ajv to v6.9.2|djmitche|N/A|2019-02-25 17:30:54|
|[Link](https://github.com/taskcluster/taskcluster/commit/2cb04cb5843f2bcbd79c1e7d251f85c01857e498)|Update dependency ajv to v6.9.2|renovate-bot|N/A|2019-02-25 00:54:11|

|	treescript	|	[MarkDown](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.md)	|	[Json](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.json)	| 
|:----------:|:-----------------------:|:--------:| 
 
| Link | Last commit | Author | Reviewer | Deploy time | 
|:----------:|:-----------:|:------:|:--------:|:-----------:| 
| |No push in the last day.. [see the history of MD commits](https://github.com/mozilla-releng/firefox-infra-changelog/blob/master/git_files/treescript.md)|FIC - BOT|Self Generated| - |
