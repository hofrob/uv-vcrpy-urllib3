Resolving the dependencies via `uv sync` installs `urllib3==1.26.20`.
While `uv pip sync` installs `urllib3==2.2.3`

# reproduce

- `uv sync --reinstall --upgrade`
- `uv pip compile --upgrade pyproject.toml --output-file requirements.txt && uv pip sync requirements.txt`

The version constraints that might be the cause of this are [here](https://github.com/kevin1024/vcrpy/blob/v6.0.2/setup.py#L29)
