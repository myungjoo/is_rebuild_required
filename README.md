# is_rebuild_required
Check if rebuild is required for GitHub Actions


# How to use

```yaml
    - uses: myungjoo/is_rebuild_required@main
      with:
        build-script: 'gbs'
        language: 'C,C++'
        head: ${{ github.event.pull_request.head.sha }}
        num-commits: ${{ github.event.pull_request.commits }}


    - name: debugging
      if: env.rebuild == '0'
      run: echo "It says NOT to rebuild!"
    - name: debugging2
      if: env.rebuild == '1'
      run: echo "It says REBUILD!"

```
