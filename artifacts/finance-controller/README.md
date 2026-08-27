# AI Finance Controller

AI Finance Controller is a frontend dashboard for autonomous, multi-source
financial reconciliation. It connects to the existing Python FastAPI backend
without changing its endpoints or implementation.

## Configure

Copy `.env.example` to `.env` and set the backend URL:

```bash
NEXT_PUBLIC_API_URL=http://localhost:8000
```

The dashboard also lets you change the backend URL at runtime. The last-used
URL is stored locally in the browser.

## Run

From the workspace root:

```bash
pnpm --filter @workspace/finance-controller run dev
```

The app targets the existing FastAPI service and uses its `/`, `/generate`,
`/reconcile`, `/status/{job_id}`, `/progress/{job_id}`, `/results/{job_id}`,
`/audit/{job_id}`, `/compare`, and `/data/*.csv` endpoints unchanged.