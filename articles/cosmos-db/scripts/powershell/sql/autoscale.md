---
title: Script de PowerShell para crear un contenedor y una base de datos de SQL API para Azure Cosmos DB con escalabilidad automática
description: 'Script de Azure PowerShell: creación de un contenedor y base de datos de SQL API para Azure Cosmos DB con escalabilidad automática'
author: markjbrown
ms.service: cosmos-db
ms.subservice: cosmosdb-sql
ms.topic: sample
ms.date: 07/30/2020
ms.author: mjbrown
ms.openlocfilehash: 66bc69bf1d81c9da9b9da4f670e9c8589c8400ed
ms.sourcegitcommit: 3bdeb546890a740384a8ef383cf915e84bd7e91e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "93102095"
---
# <a name="create-a-database-and-container-with-autoscale-for-azure-cosmos-db---sql-api"></a>Creación de una base de datos y un contenedor con escalabilidad automática para Azure Cosmos DB: SQL API
[!INCLUDE[appliesto-sql-api](../../../includes/appliesto-sql-api.md)]

[!INCLUDE [updated-for-az](../../../../../includes/updated-for-az.md)]

[!INCLUDE [sample-powershell-install](../../../../../includes/sample-powershell-install-no-ssh.md)]

## <a name="sample-script"></a>Script de ejemplo

Este script crea una cuenta de Cosmos para la API Core (SQL) en dos regiones con coherencia de nivel de sesión, una base de datos y un contenedor con una directiva de rendimiento de escalabilidad automática y de índice predeterminado.

[!code-powershell[main](../../../../../powershell_scripts/cosmosdb/sql/ps-sql-autoscale.ps1 "Create an account, database, and container with autoscale for Core (SQL) API")]

## <a name="clean-up-deployment"></a>Limpieza de la implementación

Después de ejecutar el script de ejemplo, se puede usar el comando siguiente para quitar el grupo de recursos y todos los recursos asociados.

```powershell
Remove-AzResourceGroup -ResourceGroupName "myResourceGroup"
```

## <a name="script-explanation"></a>Explicación del script

Este script usa los siguientes comandos. Cada comando de la tabla crea un vínculo a documentación específica del comando.

| Get-Help | Notas |
|---|---|
|**Azure Cosmos DB**| |
| [New-AzCosmosDBAccount](/powershell/module/az.cosmosdb/new-azcosmosdbaccount) | Crea una cuenta de Cosmos DB. |
| [New-AzCosmosDBSqlDatabase](/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase) | Crea una base de datos SQL de Cosmos DB. |
| [New-AzCosmosDBSqlContainer](/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer) | Crea un nuevo contenedor SQL de Cosmos DB. |
|**Grupos de recursos de Azure**| |
| [Remove-AzResourceGroup](/powershell/module/az.resources/remove-azresourcegroup) | Elimina un grupo de recursos, incluidos todos los recursos anidados. |
|||

## <a name="next-steps"></a>Pasos siguientes

Para más información sobre Azure PowerShell, consulte la [documentación de Azure PowerShell](/powershell/).
