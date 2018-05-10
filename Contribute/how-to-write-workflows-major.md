---
title: GitHub-Beitragsworkflow für größere oder langfristige Änderungen
description: In diesem Artikel erfahren Sie, wie Sie den Beitragsworkflow für größere Änderungen bei der Mitwirkung an docs.microsoft.com-Artikeln verwenden.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: e26b62923eed22d5b2005b1d84dc4ae240d262b1
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a><span data-ttu-id="25ae2-103">GitHub-Beitragsworkflow für größere oder langfristige Änderungen</span><span class="sxs-lookup"><span data-stu-id="25ae2-103">GitHub contribution workflow for major or long-running changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25ae2-104">Für alle Repositorys, die in „docs.microsoft.com“ veröffentlichen, gilt der Verhaltenskodex von [Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) oder von [.NET Foundation](https://dotnetfoundation.org/code-of-conduct) (beide in englischer Sprache).</span><span class="sxs-lookup"><span data-stu-id="25ae2-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="25ae2-105">Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/).</span><span class="sxs-lookup"><span data-stu-id="25ae2-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="25ae2-106">Wenden Sie sich mit Ihren Fragen oder Kommentaren alternativ an [opencode@microsoft.com](mailto:opencode@microsoft.com) oder [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).</span><span class="sxs-lookup"><span data-stu-id="25ae2-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="25ae2-107">Kleinere Korrekturen oder Klarstellungen zu Dokumentation und Codebeispielen in öffentlichen Repositorys werden durch die [docs.microsoft.com - Nutzungsbestimmungen](https://docs.microsoft.com/legal/termsofuse) abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="25ae2-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="25ae2-108">Neue oder signifikante Änderungen haben einen Kommentar im Pull Request zur Folge, in dem Sie gebeten werden, online eine Lizenzvereinbarung für Beiträge (Contribution License Agreement, CLA) zu akzeptieren. Dies gilt, wenn Sie kein Mitarbeiter von Microsoft sind.</span><span class="sxs-lookup"><span data-stu-id="25ae2-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="25ae2-109">Sie müssen das Onlineformular ausfüllen, damit wir Ihren Pull Request zusammenführen können.</span><span class="sxs-lookup"><span data-stu-id="25ae2-109">You will need to complete the online form before your pull request can be merged.</span></span>

## <a name="overview"></a><span data-ttu-id="25ae2-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="25ae2-110">Overview</span></span>

<span data-ttu-id="25ae2-111">Dieser Workflow eignet sich für Mitwirkende, die eine größere Änderung vornehmen müssen oder häufig an einem Repository mitwirken werden.</span><span class="sxs-lookup"><span data-stu-id="25ae2-111">This workflow is suitable for a contributor who needs to make a major change or will be a frequent contributor to a repository.</span></span> <span data-ttu-id="25ae2-112">Häufig Mitwirkende befassen sich in der Regel mit laufenden (langfristigen) Änderungen, die vor der Genehmigung des Pull Requests und Zusammenführung der Änderungen mehrere Build-/Validierungs-/Stagingzyklen durchlaufen oder sich über mehrere Tage erstrecken.</span><span class="sxs-lookup"><span data-stu-id="25ae2-112">Frequent contributors typically have ongoing (long-running) changes, which go through multiple build/validation/staging cycles or span multiple days before pull request sign-off and merge.</span></span>

<span data-ttu-id="25ae2-113">Zu den Beispielen für diese Arten von Beiträgen zählen:</span><span class="sxs-lookup"><span data-stu-id="25ae2-113">Examples of these types of contributions include:</span></span>

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a><span data-ttu-id="25ae2-114">Terminologie</span><span class="sxs-lookup"><span data-stu-id="25ae2-114">Terminology</span></span>

<span data-ttu-id="25ae2-115">Bevor Sie beginnen, betrachten wir einige der in diesem Workflow verwendeten Git-/GitHub-Begriffe und Moniker.</span><span class="sxs-lookup"><span data-stu-id="25ae2-115">Before you start, let's review some of the Git/GitHub terms and monikers used in this workflow.</span></span> <span data-ttu-id="25ae2-116">Es macht nichts, wenn Sie sie jetzt noch nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-116">Don't worry about understanding them now.</span></span> <span data-ttu-id="25ae2-117">Sie werden sie kennenlernen. Und sollten Sie einmal eine Definition überprüfen wollen, können Sie auf diesen Abschnitt zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-117">Just know that you will be learning about them, and you can refer back to this section when you need to verify a definition.</span></span>

| <span data-ttu-id="25ae2-118">Name</span><span class="sxs-lookup"><span data-stu-id="25ae2-118">Name</span></span> | <span data-ttu-id="25ae2-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25ae2-119">Description</span></span> |
|-----------|-------------|
|<span data-ttu-id="25ae2-120">Fork</span><span class="sxs-lookup"><span data-stu-id="25ae2-120">fork</span></span>|<span data-ttu-id="25ae2-121">Wird beim Verweis auf eine Kopie des GitHub-Repositorys normalerweise als Substantiv verwendet.</span><span class="sxs-lookup"><span data-stu-id="25ae2-121">Normally used as a noun, when referring to a copy of a main GitHub repository.</span></span> <span data-ttu-id="25ae2-122">Praktisch ist ein Fork einfach ein anderes Repository.</span><span class="sxs-lookup"><span data-stu-id="25ae2-122">In practice, a fork is just another repository.</span></span> <span data-ttu-id="25ae2-123">Aber das Besondere daran ist, dass GitHub eine Verbindung zurück zum Haupt-/übergeordneten Repository aufrechterhält.</span><span class="sxs-lookup"><span data-stu-id="25ae2-123">But it's special in the sense that GitHub maintains a connection back to the main/parent repository.</span></span> <span data-ttu-id="25ae2-124">Der Begriff wird manchmal als Verb verwendet, wie in „Sie müssen zuerst das Repositorys forken“.</span><span class="sxs-lookup"><span data-stu-id="25ae2-124">It's sometimes used as a verb, as in "You must fork the repository first."</span></span>|
|<span data-ttu-id="25ae2-125">Remote</span><span class="sxs-lookup"><span data-stu-id="25ae2-125">remote</span></span>|<span data-ttu-id="25ae2-126">Eine benannte Verbindung mit einem Remoterepository, wie ein „Origin“- oder „Uppstreamremote“.</span><span class="sxs-lookup"><span data-stu-id="25ae2-126">A named connection to a remote repository, such as the "origin" or "upstream" remote.</span></span> <span data-ttu-id="25ae2-127">Git bezeichnet diese als „Remotes“, weil sie zum Verweis auf ein Repository verwendet werden, das auf einem anderen Computer gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="25ae2-127">Git refers to these as remotes because they are used to reference a repository that's hosted on another computer.</span></span> <span data-ttu-id="25ae2-128">In diesem Workflow ist ein Remote immer ein GitHub-Repository.</span><span class="sxs-lookup"><span data-stu-id="25ae2-128">In this workflow, a remote is always a GitHub repository.</span></span>|
|<span data-ttu-id="25ae2-129">Origin</span><span class="sxs-lookup"><span data-stu-id="25ae2-129">origin</span></span>|<span data-ttu-id="25ae2-130">Der Name der Verbindung zwischen Ihrem lokalen Repository und dem Repository, von dem es geklont wurde.</span><span class="sxs-lookup"><span data-stu-id="25ae2-130">The name assigned to the connection between your local repository and the repository from which it was cloned.</span></span> <span data-ttu-id="25ae2-131">In diesem Workflow stellt Origin die Verbindung mit Ihrem Fork dar.</span><span class="sxs-lookup"><span data-stu-id="25ae2-131">In this workflow, origin represents the connection to your fork.</span></span> <span data-ttu-id="25ae2-132">Er wird manchmal als Moniker für das Ursprungsrepository selbst verwendet, wie in „Denken Sie daran, Ihre Änderungen an Origin zu pushen“.</span><span class="sxs-lookup"><span data-stu-id="25ae2-132">It's sometimes used as a moniker for the origin repository itself, as in "Remember to push your changes to origin."</span></span>|
|<span data-ttu-id="25ae2-133">Upstream</span><span class="sxs-lookup"><span data-stu-id="25ae2-133">upstream</span></span>|<span data-ttu-id="25ae2-134">Wie Originremote ist Upstream eine benannte Verbindung mit einem anderen Repository.</span><span class="sxs-lookup"><span data-stu-id="25ae2-134">Like the origin remote, upstream is a named connection to another repository.</span></span> <span data-ttu-id="25ae2-135">In diesem Workflow stellt Upstream die Verbindung zwischen Ihrem lokalen Repository und dem Hauptrepository dar, aus dem Ihr Fork erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="25ae2-135">In this workflow, upstream represents the connection between your local repository and the main repository, from which your fork was created.</span></span> <span data-ttu-id="25ae2-136">Der Begriff wird manchmal als Moniker für das Upstreamrepository selbst verwendet, wie in „Denken Sie daran, Ihre Änderungen vom Upstream zu pullen.“</span><span class="sxs-lookup"><span data-stu-id="25ae2-136">It's sometimes used as a moniker for the upstream repository itself, as in "Remember to pull the changes from upstream."</span></span>|

## <a name="workflow"></a><span data-ttu-id="25ae2-137">Workflow</span><span class="sxs-lookup"><span data-stu-id="25ae2-137">Workflow</span></span>

>[!IMPORTANT]
> <span data-ttu-id="25ae2-138">Falls nicht bereits geschehen, müssen Sie die im Bereich [Setup](get-started-setup-github.md) beschriebenen Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-138">If you haven't already, you must complete the steps in the [Setup](get-started-setup-github.md) section.</span></span> <span data-ttu-id="25ae2-139">Dieser Abschnitt führt Sie durch die Einrichtung Ihres GitHub-Kontos, wobei Git Bash und ein Markdown-Editor installiert, ein Fork erstellt und Ihr lokales Repository eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="25ae2-139">This section walks you through setting up your GitHub account, installing Git Bash and a Markdown editor, creating a fork, and setting up your local repository.</span></span> <span data-ttu-id="25ae2-140">Wenn Sie mit Git- und GitHub-Konzepten wie Repository oder Branch nicht vertraut sind, lesen Sie bitte zuerst [Git and GitHub essentials (Git- und GitHub-Grundlagen)](git-github-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="25ae2-140">If you are unfamiliar with Git and GitHub concepts such as a repository or branch, please first review [Git and GitHub fundamentals](git-github-fundamentals.md).</span></span>

<span data-ttu-id="25ae2-141">In diesem Workflow fließen Änderungen in einen Wiederholungszyklus ein.</span><span class="sxs-lookup"><span data-stu-id="25ae2-141">In this workflow, changes flow in a repetitive cycle.</span></span> <span data-ttu-id="25ae2-142">Vom lokalen Repository Ihres Geräts fließen sie zurück zu Ihrem GitHub-Fork, in das GitHub-Hauptrepository und wieder zum lokalen Repository zurück, während Sie Änderungen anderer Mitwirkender einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-142">Starting from your device's local repository, they flow back up to your GitHub fork, into the main GitHub repository, and back down locally again as you incorporate changes from other contributors.</span></span>

### <a name="use-github-flow"></a><span data-ttu-id="25ae2-143">Verwenden des GitHub-Flows</span><span class="sxs-lookup"><span data-stu-id="25ae2-143">Use GitHub flow</span></span>

<span data-ttu-id="25ae2-144">In [Git and GitHub essentials (Git- und GitHub-Grundlagen)](git-github-fundamentals.md#git) haben Sie gelernt, dass ein Git-Repository einen Masterbranch sowie einige zusätzliche Branches in Bearbeitung enthält, die nicht in den Masterbranch integriert wurden.</span><span class="sxs-lookup"><span data-stu-id="25ae2-144">Recall from [Git and GitHub fundamentals](git-github-fundamentals.md#git) that a Git repository contains a master branch, plus any additional work-in-progress branches that have not been integrated into master.</span></span> <span data-ttu-id="25ae2-145">Immer dann, wenn Sie mehrere logisch verknüpfte Änderungen vornehmen, sollten Sie einen *Arbeitsbranch* erstellen, um Ihre Änderungen über den Workflow zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="25ae2-145">Whenever you introduce a set of logically related changes, it’s a best practice to create a *working branch* to manage your changes through the workflow.</span></span> <span data-ttu-id="25ae2-146">Wir verwenden hier die Bezeichnung Arbeitsbranch, weil es sich um einen Arbeitsbereich zum Durchlaufen bzw. Optimieren von Änderungen handelt, bis diese wieder in den Masterbranch integriert werden können.</span><span class="sxs-lookup"><span data-stu-id="25ae2-146">We refer to it here as a working branch because it's a workspace to iterate/refine changes, until they can be integrated back into the master branch.</span></span>

<span data-ttu-id="25ae2-147">Mit der Isolation zugehöriger Änderungen in einem bestimmten Branch können Sie diese Änderungen unabhängig steuern und einführen und zu einem bestimmten Zeitpunkt im Veröffentlichungszyklus freigeben.</span><span class="sxs-lookup"><span data-stu-id="25ae2-147">Isolating related changes to a specific branch allows you to control and introduce those changes independently, targeting them to a specific release time in the publishing cycle.</span></span> <span data-ttu-id="25ae2-148">Sie könnten abhängig vom Typ Ihrer Arbeit mühelos über mehrere Arbeitsbranches in Ihrem Repository verfügen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-148">In reality, depending on the type of work you do, you can easily end up with several working branches in your repository.</span></span> <span data-ttu-id="25ae2-149">Es ist nicht ungewöhnlich, mit mehreren Branches gleichzeitig zu arbeiten, wobei jeder Branch für ein Projekt steht.</span><span class="sxs-lookup"><span data-stu-id="25ae2-149">It's not uncommon to be working on multiple branches at the same time, each representing a different project.</span></span>

>[!TIP]
><span data-ttu-id="25ae2-150">Änderungen im Masterbranch vorzunehmen, ist *keine* bewährte Methode.</span><span class="sxs-lookup"><span data-stu-id="25ae2-150">Making your changes in the master branch is *not* a good practice.</span></span> <span data-ttu-id="25ae2-151">Stellen Sie sich vor, Sie wurden den Masterbranch verwenden, um mehrere Änderungen für die Freigabe von Features zu einem bestimmten Zeitpunkt einzuführen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-151">Imagine that you use the master branch to introduce a set of changes for a timed feature release.</span></span> <span data-ttu-id="25ae2-152">Sie schließen die Änderungen ab und warten auf ihre Freigabe.</span><span class="sxs-lookup"><span data-stu-id="25ae2-152">You finish the changes and are waiting to release them.</span></span> <span data-ttu-id="25ae2-153">Dann erhalten Sie in der Zwischenzeit die dringende Anfrage, ein Problem zu beheben, also nehmen Sie die Änderung in einer Datei im Masterbranch vor und veröffentlichen dann die Änderung.</span><span class="sxs-lookup"><span data-stu-id="25ae2-153">Then in the interim, you have an urgent request to fix something, so you make the change to a file in the master branch and then publish the change.</span></span> <span data-ttu-id="25ae2-154">In diesem Beispiel veröffentlichen Sie unabsichtlich die Problembehebung *und* die Änderungen, die Sie zur Freigabe zu einem bestimmten Datum zurückgehalten haben.</span><span class="sxs-lookup"><span data-stu-id="25ae2-154">In this example, you inadvertently publish both the fix *and* the changes that you were holding for release on a specific date.</span></span>

<span data-ttu-id="25ae2-155">Nun erstellen wir einen neuen Arbeitsbranch in Ihrem lokalen Repository, um die von Ihnen vorgeschlagenen Änderungen zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="25ae2-155">Now let's create a new working branch in your local repository, to capture your proposed changes.</span></span> <span data-ttu-id="25ae2-156">Jeder Git-Client ist anders, informieren Sie sich also in der Hilfe über die Anforderungen für Ihren bevorzugten Client.</span><span class="sxs-lookup"><span data-stu-id="25ae2-156">Each git client is different, so consult the help for your preferred client.</span></span> <span data-ttu-id="25ae2-157">Eine Übersicht über den Prozess finden Sie im GitHub-Leitfaden unter [GitHub-Flow](https://guides.github.com/introduction/flow/) (in englischer Sprache).</span><span class="sxs-lookup"><span data-stu-id="25ae2-157">You can see an overview of the process in the GitHub Guide on [GitHub flow](https://guides.github.com/introduction/flow/).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="25ae2-158">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="25ae2-158">Next steps</span></span>

<span data-ttu-id="25ae2-159">Das ist alles!</span><span class="sxs-lookup"><span data-stu-id="25ae2-159">That's it!</span></span> <span data-ttu-id="25ae2-160">Sie haben einen Beitrag zum Inhalt von docs.microsoft.com geleistet!</span><span class="sxs-lookup"><span data-stu-id="25ae2-160">You've made a contribution to docs.microsoft.com content!</span></span>

- <span data-ttu-id="25ae2-161">Fahren Sie mit dem Abschnitt zu Schreibgrundlagen fort, um u.a. mehr über Themen wie Markdown und Markdownerweiterungssyntax zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="25ae2-161">To learn more about topics such as Markdown and Markdown extensions syntax, continue to the "Writing essentials" section.</span></span>