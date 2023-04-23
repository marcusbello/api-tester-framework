# API Testing framework
### How to run
`````# Setup report portal on docker
# Update rp_uuid in pytest.ini with project token
docker-compose -f docker-compose.yml -p reportportal up -d

# Launch pipenv
pipenv shell

# Install all packages
pipenv install

# Run tests via pytest (single threaded)
python -m pytest

# Run tests in parallel
python -m pytest -n auto

# Report results to report portal
python -m pytest -n auto ./tests --reportportal