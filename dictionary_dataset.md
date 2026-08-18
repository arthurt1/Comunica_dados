# A Dataset of 10-Year Bug-Fixing in the Apache Hadoop Project

Este dataset foi utilizado na pesquisa publicada em [1] e consiste em um conjunto de tarefas de correção de bugs no projeto [Apache Hadoop](https://hadoop.apache.org/), coletadas ao longo de um período de `10` anos. Além disso, o dataset foi manualmente rotulado para indicar se o bug registrado é ou não um bug de tratamento de exceção.

```bash
[1] da Silva, A.J.A., Vieira, R.G., Mesquita, D.P.P. et al. Towards automatic labeling of exception handling bugs: A case study of 10 years bug-fixing in Apache Hadoop. Empir Software Eng 29, 85 (2024). https://doi.org/10.1007/s10664-024-10494-0
```

A tabela abaixo detalha cada campo do dataset:

| Field                     | From | Type       | Description                                                                                       |
|---------------------------|------|------------|---------------------------------------------------------------------------------------------------|
| Project                   | Jira | General    | The project to which the bug belongs                                                              |
| Owner                     | Jira | General    | The owner/maintainer of the project                                                               |
| Manager                   | Jira | General    | The committee responsible for the project                                                         |
| Category                  | Jira | General    | The project domain category                                                                       |
| Key                       | Jira | General    | A unique identifier for the bug                                                                   |
| Priority                  | Jira | General    | The importance of the issue in relation to other issues.                                          |
| Status                    | Jira | General    | The stage the bug is currently at in its lifecycle                                                |
| Reporter                  | Jira | General    | The person who entered the bug into the system                                                    |
| Assignee                  | Jira | General    | The person who was assigned to fix the bug                                                        |
| Components                | Jira | General    | The project component(s) to which the bug relates                                                 |
| SummaryTopWords           | Jira | Text       | 1000 top most frequent words of a brief one-line summary of the bug                               |
| DescriptionTopWords       | Jira | Text       | 1000 top most frequent words of a detailed description of the bug                                 |
| CommentTopWords           | Jira | Text       | 1000 top most frequent words of the comments of the bug                                           |
| CreationDate              | Jira | Time       | The date and time on which the bug was entered into Jira                                          |
| ResolutionDate            | Jira | Time       | The date and time on which the bug was resolved                                                   |
| LastUpdateDate            | Jira | Time       | The date and time on which the bug report was updated for the last time                           |
| AffectsVersions           | Jira | Versioning | The project version(s) for which the bug is (or was) manifesting                                  |
| FixVersions               | Jira | Versioning | The project version(s) in which the bug was (or will be) fixed                                    |
| NoComments                | Jira | Summation  | The number of all comments added in the bug                                                       |
| FirstCommentDate          | Jira | Time       | The date and time on which the first comment was added in the bug report                          |
| LastCommentDate           | Jira | Time       | The date and time on which the last comment was added in the bug report                           |
| NoWatchers                | Jira | Summation  | The number of how many people are watching (interested in) the bug                                |
| NoAttachments             | Jira | Summation  | The number of attachments (documents, images, screenshots) added in the bug report                |
| FirstAttachmentDate       | Jira | Time       | The date and time on which the first attachment was added                                         |
| LastAttachmentDate        | Jira | Time       | The date and time on which the last attachment was added                                          |
| NoAttachedPatches         | Jira | Summation  | The number of patches added to the bug                                                            |
| FirstAttachedPatchDate    | Jira | Time       | The date and time on which the first patch was attached                                           |
| LastAttachedPatchDate     | Jira | Time       | The date and time on which the last patch was attached                                            |
| NoInwardIssueLinks        | Jira | Link       | The issue on which the bug depends on (type: inwardIssue).                                        |
| OutwardIssueLinks         | Jira | Link       | The issue that depends on the bug (type: outwardIssue).                                           |
| HasMergeCommit            | Git  | General    | This field informs whether a bug fix had or not a merge commit                                    |
| CommitsMessagesTopWords   | Git  | Text       | 1000 top most frequent words of the commit messages related to the bug                            |
| NoCommits                 | Git  | Summation  | The number of commits related to the bug                                                          |
| NoAuthors                 | Git  | Summation  | The number of different authors who performed commits related to the bug                          |
| NoCommitters              | Git  | Summation  | The number of different committers who performed commits related to the bug                       |
| AuthorsFirstCommitDate    | Git  | Time       | The date and time on which the author performed the first commit to fix the bug                   |
| AuthorsLastCommitDate     | Git  | Time       | The date and time on which the author performed the last commit to fix the bug                    |
| CommittersFirstCommitDate | Git  | Time       | The date and time on which the committer performed the first commit to fix the bug                |
| CommittersLastCommitDate  | Git  | Time       | The date and time on which the committer performed the last commit to fix the bug                 |
| NoSrcAddFiles             | Git  | SRC  | The number of ource code files added by commits related to the bug                           |
| NonSrcAddFiles            | Git  | SRC        | The number of non-source code files added by commits related to the bug                           |
| NonSrcDelFiles            | Git  | SRC        | The number of non-source code files deleted by commits related to the bug                         |
| NonSrcModFiles            | Git  | SRC        | The number of non-source code files modified by commits related to the bug                        |
| NonSrcAddLines            | Git  | SRC        | The number of non-source code lines added by commits related to the bug                           |
| NonSrcDelLines            | Git  | SRC        | The number of non-source code lines deleted by commits related to the bug                         |
| SrcAddFiles               | Git  | SRC        | The number of source code files added by commits related to the bug                               |
| SrcDelFiles               | Git  | SRC        | The number of source code files deleted by commits related to the bug                             |
| SrcModFiles               | Git  | SRC        | The number of source code files modified by commits related to the bug                            |
| SrcAddLines               | Git  | SRC        | The number of source code lines added by commits related to the bug                               |
| SrcDelLines               | Git  | SRC        | The number of deleted source code lines by commits related to the bug                             |
| TestAddFiles              | Git  | SRC        | The number of source code test files added by commits related to the bug                          |
| TestDelFiles              | Git  | SRC        | The number of source code test files deleted by commits related to the bug                        |
| TestModFiles              | Git  | SRC        | The number of source code test files modified by commits related to the bug                       |
| TestAddLines              | Git  | SRC        | The number of source code test lines added by commits related to the bug                          |
| TestDelLines              | Git  | SRC        | The number of source code test lines deleted by commits related to the bug                        |
| Type                      | N/A  | N/A        | The label: `1` indicates an exception handling bug; `0` otherwise.                                |