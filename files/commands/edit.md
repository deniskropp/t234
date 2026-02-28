# Edit Command

The `edit` command facilitates the modification of workspace files and knowledge items, ensuring consistency with the project's architectural standards.

## Usage

```bash
python -m src.cli edit [PATH] [OPTIONS]
```

## Parameters

- `path`: The target file path or resource identifier.
- `--content`: The new content to be applied.
- `--git-move`: If specified, uses `git mv` for path changes.

## Implementation Details

The command utilizes `src.shared.services.EditService` for business logic and `src.shared.models.EditRequest` for Pydantic v2 validation.

### Async Example

```python
from typing import Annotated
from pathlib import Path
from src.shared.models import EditRequest
from src.shared.services import edit_service

async def perform_edit(path: Path, content: str) -> None:
    """Asynchronously applies edits to a target file."""
    request = EditRequest(path=path, content=content)
    await edit_service.apply(request)
```

## Blueprint (.kl)

```kicklang
blueprint EditCommand {
    target: Path
    content: String
    validate: Boolean = true
}
```
