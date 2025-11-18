# diabetes-indicator-api
API for the Diabetes Indicator App -> [kmads.dev/github/diabetes-indicator](https://kmads.dev/diabetes-indicator/)<br>
Acess the diabetes-indicator repository here: [kmads.dev/source-code/diabetes-indicator](https://kmads.dev/diabetes-indicator)

```
    diabetes-indicator-api
    ⊢ api/
    |  ⊢ app.py (running on vercel, fastapi + uvicorn)
    |  ⌞ requirements.txt (dependencies to deploy the api)
    |
    ⊢ trainedModels/ 
    |  ⌞ <.pkl files>
    |
    ⌞ README, LICENSE, ...
```

### Infra / Architecture
- **Frontend:** `kmadsdev/diabetes-indicator/docs`
- **Backend:** `kmadsdev/diabetes-indicator-api/api`
- **Machine Learning:** `kmadsdev/diabetes-indicator/predictionModel` & `kmadsdev/diabetes-indicator-api/trainedModels`

Architecture:
- ***`Client`*** Request request prediction from ***`docs/` (github pages)*** 
- ***`docs/` (github pages)*** gets prediction from ***`api/` (vercel)***
- ***`api/` (vercel)*** gets the latest model (.pkl) model from ***`trainedModels/` (github)***
- ***`trainedModels/` (github)*** gets the model (.pkl) from ***`predictionModel/` (github)***

Simplified: <br>
- Client -> Frontend (docs/) -> Backend (api/) <br> 
- Backend (api/) -> model.pkl (trainedModels/) -> ml.ipynb (predictionModel/)

![Architecture](https://raw.githubusercontent.com/kmadsdev/diabetes-indicator/main/assets/infra/architecture-2025-11-18.svg)
