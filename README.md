# setup-cgbpf

Set up your GitHub Actions workflow for [CG-BPF](https://github.com/JavidDitty/cintent).

## Usage

```yaml
steps:
- uses: actions/checkout@v4

- uses: JavidDitty/setup-cgbpf@v1

# Insert your other steps here

- name: Upload CG-BPF Artifacts
  uses: actions/upload-artifact@v4
  if: always()
  with:
    name: ${{ env.CGBPF_ARTIFACT_NAME }}
    path: ${{ env.CGBPF_LOGS }}
```
