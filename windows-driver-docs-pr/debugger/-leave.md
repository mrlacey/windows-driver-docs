---
title: .leave (WinDbg)
description: The .leave token is used to exit from a .catch block.
keywords: [".leave Windows Debugging"]
ms.date: 05/23/2017
topic_type:
- apiref
api_name:
- .leave
api_type:
- NA
---

# .leave


The **.leave** token is used to exit from a [**.catch**](-catch.md) block.

```dbgcmd
.catch { ... ; .if (Condition) .leave ; ... } 
```

## <span id="ddk_token_leave_dbg"></span><span id="DDK_TOKEN_LEAVE_DBG"></span>


### <span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>Additional Information

For information about other control flow tokens and their use in debugger command programs, see [Using Debugger Command Programs](using-debugger-command-programs.md).

## Remarks

When a **.leave** token is encountered within a [**.catch**](-catch.md) block, the program exits from the block, and execution resumes with the first command after the closing brace.

Since there is no control flow token equivalent to the C **goto** statement, you will usually use the **.leave** token within an [**.if**](-if.md) conditional, as shown in the syntax examples above. However, this is not actually required.

 

 





