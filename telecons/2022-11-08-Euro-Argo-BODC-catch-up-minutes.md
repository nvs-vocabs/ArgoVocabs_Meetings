#### 1) Blockers to implementing Argo NVS collections into the GDAC file checker

Technical parameter names and Configuration parameter names tables need to be on the NVS. These are the last two tables that need transferring onto the NVS before the GDAC file checker can plug the Argo NVS collections in.

Given the blocker status and the urgency of rolling out the updated GDAC file checker version, the following options have been proposed:

a. Transfer the tech. and config. parameter names tables onto the NVS as they are, and review later (inc. deprecating terms if necessary)

b. Transfer only terms deemed as 'mandatory' (and that would therefore be rejected if non-compliant), then review, then tackle the 'optional' terms (that would warrant a 'warning' from the GDAC file checker)

c. Review terms that apply to live floats, then transfer to the NVS - repeat the process in phases until all legacy terms are reviewed and transferred to the NVS

Option a) would be the quickest. There are some questions on whether the integrity of the NVS could be compromised if new concepts were created before having been reviewed first.

Option b) could be a compromise, as a smaller number of un-reviewed terms would be transferred compared to option a). We would need to assess how many terms are considered mandatory vs optional in the GDAC file checker.

Option c) is the option that had been discussed and agreed with the AVTT members responsible for these tables. It would take longer than option a), but all terms on the NVS would have been reviewed.

To note: the AVTT editor responsible for the configuration parameter names table is stepping aside from this role, and a new person will be sought to replace them. Euro-Argo offered to be involved in this work, however a supplementary person with a good knowledge of these terms (from a DAC) would still be needed.

The CONTROLLER_BOARD_PRIMARY table (R28) was not being checked by the GDAC file checker before, so wouldn't be a blocker now. BODC has been reviewing this table ahead of tranfer to the NVS. Euro-Argo suggested transferring what is currently on the spreadsheet to the NVS directly - BODC will check the current status of this work before deciding.

#### 2) Workflow for the creation and updates of metadata tables (legacy spreadsheet documents) and NVS collections (while the two systems co-exist and after)

We reminded ourselves of the workflow agreed: The AVTT team on GitHub and its organisation into separate groups/sub-teams, responsible for a specific set of vocabularies. The GitHub is the main forum for AVTT/ADMT, and is the gateway to NVS updates. For collection-specific queries, discussions, updates etc., new issues can be opened in the appropriate repository (see list). For general Argo vocabularies discussions, the ArgoVocabs repository can be used, which is linked to the whole AVTT. Editors are illustrated in the AVTT GitHub home page (https://github.com/orgs/nvs-vocabs/teams/avtt). They should have permission to edit specific Argo NVS collections. The 'edit' is done through the BODC Vocabulary Editor: https://www.bodc.ac.uk/resources/vocabularies/vocabulary_editor/. Once submitted, edits are reviewed by an NVS gatekeeper on the BODC side. 

It was noticed that the NVS Editors web interface was not working properly this afternoon - collection-specific editors pages would not load. Update: this could be due to changes in permission.

Unfortunately, due to lack of training/clarity on the workflow as well as being under-resourced, the legacy spreadsheet documents have been updated instead of the corresponding live NVS collections. This has happened for SENSOR_MODEL. If training/clarity/continuous support is not achieved, we risk a permanent mis-match between the legacy spreadsheets and the NVS, which defies the effort of having the NVS collections as the 'master' source of the metadata lists for Argo (and their linkage with the GDAC file checker).

Euro-Argo also raises this point as a supplementary motivation to choose option a) for tackling Technical parameter names and Configuration parameter names tables: if the file checker is plugged in with the NVS then, consequently, the NVS will be kept up-to-date.

#### 3) Continuous NVS support: what has been planned? how to ensure it?

The Argo NVS GitHub space was designed with the assumption that AVTT members, once allocated to a specific sub-team (e.g. 'Reference Tables'), would be automatically notified at every issue update/creation in one of the repositories linked to their sub-team. However, this is not an in-built GitHub functionality, meaning that each AVTT members would have to manually activate the 'watch' feature in every single repository they are responsible for. AVTT members have been prompted to do this in the past, however it is recognised this is not a very efficient way of monitoring the GitHub space.

In our meeting, it was suggested to have one Repository for each sub-team, or just a single repository to log issues to (e.g. the existing https://github.com/nvs-vocabs/ArgoVocabs one), and assign labels to clarify which NVS collections those issues refer to. This solution would be more pragmatic also because it would allow issues to encompass more than one collection - this is not possible now, because each collection corresponds to a unique repository (e.g. the R27 NVS collection has its own R27 repository, as linked in the R27 NVS collection interface itself: https://vocab.nerc.ac.uk/search_nvs/R27/?searchstr=&options=identifier,preflabel,altlabel,status_accepted&rbaddfilter=inc&searchstr2= (see 'External link), or https://vocab.nerc.ac.uk/collection/R27/current/ under 'See also'. Moreover, some Argo NVS collections are much more active than others - some rarely need updates and are more static, possibly rendering their unique GitHub repository redundant or of not much use compared to others.

Targeted, effective training is key to ensure that the AVTT editors know how to edit existing NVS collections through the Vocabulary Editor tool: https://www.bodc.ac.uk/resources/vocabularies/vocabulary_editor/. 

The issue of funding and resource to support this infrastructure was also raised: over the past 14+ months, BODC Argo has been going through difficulties due to under-staffing and running out of critical funding, which has had an impact on progress on the Argo NVS side. BODC currently only has allocated Argo NVS funding until spring 2023, and a forward plan has to be put in place to ensure continuity among the Argo community.

#### 4) Euro-Argo involvement (e.g. active part in AVTT github issues, check fields population in the process of new table creation, etc.)
Euro-Argo is very happy to stay involved in this work.

#### 5) Unconstrained fileds FLOAT_OWNER, OPERATING_INSTITUTION, PROJECT_NAME
Several meetings between Euro-Argo, BODC and OceanOps have taken place in early 2022. A record of these is stored at the three organisations. No meetings have been held since April 2022 though, and it would be good to re-instate them.

In April 2022, two new collections were proposed: PROGRAM (list of national Argo programs as in https://www.ocean-ops.org/api/1/help/?param=program) and PROJECT to remain free text. This can be followed here: https://github.com/nvs-vocabs/ArgoVocabs/issues/5 - no consensus has been reached yet.

#### 6) Miscellaneous
Legacy terms: these are metadata terms that were used in older floats and that are no longer in use. On the NVS, these terms can be deprecated - would the file checker still have access to them? would they still be visible to the ADMT/AVTT community on the NVS? It is important that these terms are still visible/accessible, but that they are clearly marked as 'phased out' and not currently in use.

Update: deprecated terms are still visible on the NVS, and are clearly marked with a 'Deprecated' sign, visible also under 'notes'. Example: http://vocab.nerc.ac.uk/collection/R11/current/11/. In VocPrez, both current and deprecated terms are visible: http://vocab.nerc.ac.uk/collection/R11/current/ (see ID 10 and 11). This distinction also exists in a machine-readable format too: http://vocab.nerc.ac.uk/collection/R11/current/11/?_profile=nvs&_mediatype=text/turtle. If a 
term is deprecated and is replaced by a new one, 'isReplacedBy' can also be added to link to the new term.

We will meet again the week after the ADMT, at least to speak about decisions that will be made at the ADMT, and update the actions with regards to that.
