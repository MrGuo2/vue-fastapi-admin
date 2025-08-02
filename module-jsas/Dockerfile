FROM python:3.12

RUN pip install --no-cache-dir uv

WORKDIR /opt/usr/moddule-jsas

COPY pyproject.toml ./
COPY uv.lock ./
COPY src ./

RUN uv pip sync --system uv.lock


EXPOSE 9999

CMD ["source", "./.venv/bin/activate"]
CMD ["python", "./src/jsas-service/run.py"]