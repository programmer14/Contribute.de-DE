---
title: ms-author-invalid
description: Erklärung und Lösung zu Problemen beim Erstellen von Dokumentationsartikeln – ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987765"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

**Bald verfügbar!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Vorschlag

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Lösung

Überprüfen Sie, dass es sich bei dem Wert `ms.author` um einen gültigen Microsoft-Alias handelt. Wenn der Alias eine Verteilerliste ist, muss dieser sich ebenfalls auf der Zulassungsliste befinden.

Gültige Werte für Verteilerlisten finden Sie auf dieser [internen Microsoft-Website](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
