# Samples

- [Basic consumption](basic/application.norm): seed configuration, read-only consumption, live switching and local scope inheritance.
- [Desktop integration](desktop/application.norm): a separate module with its own JDK Swing host. Consumes the packaged `ui.theme` archive, preserving input text and selection while changing mode and brand.
- [Desktop acceptance](desktop/tests/desktop_test.norm): real button events, local dark-scope retention and a rendered preview at `build/desktop-preview.png`.

Install the compiler selected by the [workflow](../.github/workflows/verify.yml). Run `norm run samples/basic` for the published-package example. The desktop host requires JDK 21 and PowerShell 7. Use `-Source` only when validating this checkout; see [development](../README.md#development).

```powershell
./scripts/desktop.ps1
./scripts/desktop.ps1 -Verify
```

The sample host exists only to demonstrate the adapter boundary. It is not exported by `ui.theme` and adds no UI dependencies to the core package.
