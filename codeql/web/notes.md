- By adding a simple c# project (csproj) and then adding a Web.config, that is enough to trigger codeql to run (default config can pick c# out on github repo security tab)... TBD if the Web.config as is will be reported as an issue:

BTW
- rules that copilot can address: https://docs.github.com/en/code-security/code-scanning/managing-your-code-scanning-configuration/csharp-built-in-queries
  - all supported languages: https://docs.github.com/en/code-security/code-scanning/managing-your-code-scanning-configuration/codeql-query-suites#query-lists-for-the-default-query-suites
- trying to trigger this security alert:
  - https://codeql.github.com/codeql-query-help/csharp/cs-web-directory-browse-enabled/
    - query: https://github.com/github/codeql/blob/main/csharp/ql/src/Security%20Features/CWE-548/ASPNetDirectoryListing.ql
        - yup this even shows "enabled" ... hopefully that fixes it
  - ok I got an alert but for a diff reason,one that isn't supported by copilot autofix


