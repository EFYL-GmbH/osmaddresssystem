# osmaddresssystem

Turn an OpenStreetMap road network into an address system: street identities, street direction, house numbering,
sub-street (alley) names, geocoding maps and street signs.

The package was developed with a university as part of the Community Addressing Cameroon work and is open source
under the [MIT licence](LICENSE).

## What it does

| Module | Purpose |
|---|---|
| `street_ids.py`, `branches.py` | Group road segments into streets and give each a stable identity; alleys branch off a parent street. |
| `street_direction.py`, `routing.py` | Direction of each street from a reference point. |
| `numbering.py`, `path_numbering.py` | House numbers from the distance along the street; odd on the left, even on the right. |
| `naming_plan.py`, `name_matching.py` | Which streets need a name, and matching of existing names. |
| `geocode_map.py`, `street_editor.py`, `street_signs.py`, `poi_signs.py` | Maps, an editor view and sign plans. |
| `pipeline.py`, `osm.py`, `subregions.py` | Download and process a whole area end to end. |

## Install

```bash
uv sync --extra planning        # or: pip install -e ".[planning]"
```

Python 3.11 or later.

## Examples

- `examples/tutorial/`: three notebooks (street identity, radial numbering, grid numbering).
- `examples/nuevos_ministerios/`: a Madrid example.
- `experiments/Bandja`, `experiments/Douala`: full runs on Cameroonian towns.

## Tests

```bash
uv run pytest -p no:cacheprovider
```

## Credits

- Original author: **Miguel Ureña Pliego**.
- Contributors: **Loryan Mbassi** and the Community Addressing Cameroon team.
- Map data © OpenStreetMap contributors (ODbL).

## Licence

[MIT](LICENSE).
