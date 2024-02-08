# is_rebuild_required
Check if rebuild is required for GitHub Actions


# How to use

Note that this works ONLY with pull-request events

```yaml
    - uses: myungjoo/is_rebuild_required@main
      with:
        build-script: 'gbs'

    - name: debugging
      if: env.rebuild == '0'
      run: echo "It says NOT to rebuild!"
    - name: debugging2
      if: env.rebuild == '1'
      run: echo "It says REBUILD!"

```
