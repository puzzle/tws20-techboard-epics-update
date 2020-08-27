---
title: Techboard Epics Update
---

<!-- .slide: class="master01" -->

# Techboard Epics Update

---

<!-- .slide: class="master02" -->
# Epic 1: Docs

---

<!-- .slide: class="text-left" -->
## Title

* Point 1
* Point 2

---

<!-- .slide: class="master02" -->
# Epic 2: Pipelines

---
<!-- .slide: class="text-left" -->
## Jenkins OpenShift Operator

* Syncs tokens of service accounts into Jenkins
* Grants edit rights to these service accounts

&nbsp; &nbsp; &rArr; Projects can use own SAs in pipelines

---
<!-- .slide: class="text-left" -->
## Jenkins OpenShift Operator

* Enables namespace for Jenkins OpenShift Sync

&nbsp; &nbsp; &rArr; Trigger Jenkins pipelines from OpenShift <br/> 
&nbsp; &nbsp; &rArr; Configure pipelines, credentials & slaves in <br/>
&nbsp; &nbsp; <span style="visibility: hidden">&rArr;</span> OpenShift

Documentation: [Puzzle Jenkins Developer Guide](https://wiki.puzzle.ch/Puzzle/JenkinsDeveloperGuide#OpenShift_Client_Plugin)

---
<!-- .slide: class="text-left" -->
## Puzzle Jenkins Shared Library

New Steps:

<dl>
<dt>kustomize</dt>
<dd>Generates OpenShift objects with kustomize.</dd>
<dt>openshiftApply</dt>
<dd>Applies OpenShift objects to cluster, <br/>prunes removed/renamed objects.</dd>

---
<!-- .slide: class="text-left" -->
## Puzzle Jenkins Shared Library

<dt>openshiftDiff</dt>
<dd>Diffs OpenShift objects against cluster.</dd>
<dt>replaceFromVault</dt>
<dd>Replaces variables in strings with Vault secrets.</dd>
<dt>withGitCrypt</dt>
<dd>Unlocks repo with git-crypt within scope of step.</dd>
</dl>

---
<!-- .slide: class="text-left" -->
## Example Pipelines

* [pitc-wekan-cicd-pipeline](https://jenkins.puzzle.ch/view/pitc-tb-pipelines/job/pitc-wekan-cicd-pipeline/)
* [pitc-pipeline-quickstarts-kustomize](https://jenkins.puzzle.ch/view/pitc-tb-pipelines/job/pitc-pipeline-quickstarts-kustomize/)

---
<!-- .slide: class="text-left" -->
## What's Next

* Review and merge branch
* Write documentation
* Steps and examples for Helm and ArgoCD
* Versioning and promotion
* Images and library for GitLab
* [Wekan Board](https://wekan.puzzle.ch/b/NTF72iW8TBzxa7D9Z/technical-board)
