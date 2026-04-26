# Phase 2: Configuration & First FastAPI Endpoint

## 🎯 What You'll Build in Phase 2

This phase focuses on setting up the basic FastAPI application structure with async support.

### Tasks:
1. Create virtual environment and install dependencies
2. Create config.py with environment settings
3. Create app/main.py with FastAPI app factory
4. Create app/database.py with async database setup
5. Create run.py as development entry point
6. Build first endpoint: GET /api/health
7. Test with Swagger UI

## 📋 Phase 2 Detailed Checklist

### 2.1 Virtual Environment & Dependencies
- [ ] Create venv: `python -m venv venv`
- [ ] Activate venv
- [ ] Install all packages: `pip install -r requirements.txt`
- [ ] Verify FastAPI and SQLAlchemy versions

### 2.2 Create config.py
**What to implement:**
- Database URL configuration (from environment variables)
- JWT secret keys
- Environment detection (dev/prod)
- CORS origins
- Debug mode settings
- Use os.getenv() for secrets (never hardcode)

### 2.3 Create app/main.py
**What to implement:**
- Import FastAPI
- Create FastAPI app instance with title/description/version
- Create async health check endpoint: GET /api/health
- Return JSON: {"status": "healthy", "version": "1.0.0"}

### 2.4 Create app/database.py
**What to implement:**
- Import from sqlalchemy.ext.asyncio
- Create async engine with asyncpg driver
- Create async sessionmaker
- Create get_db() async dependency
- Use DATABASE_URL from config

### 2.5 Create run.py
**What to implement:**
- Import uvicorn
- Import app from app.main
- Create main entry point
- Run uvicorn with reload=True for development

### 2.6 Create .env
- [ ] Copy from .env.example: `cp .env.example .env`
- [ ] Set DATABASE_URL (can use dummy value for now)
- [ ] Set SECRET_KEY and JWT_SECRET_KEY

### 2.7 Test Locally
- [ ] Run: `python run.py`
- [ ] Visit http://localhost:8000/docs
- [ ] See Swagger UI with health endpoint
- [ ] Test GET /api/health
- [ ] Get response: {"status": "healthy", "version": "1.0.0"}

### 2.8 Git & Push
- [ ] Commit changes: `git add . && git commit -m "feat: Add FastAPI setup with health endpoint"`
- [ ] Push: `git push origin main`

## ✅ Success Criteria

When Phase 2 is complete, you should have:
- ✅ Virtual environment set up
- ✅ All dependencies installed
- ✅ config.py with configuration
- ✅ app/main.py with FastAPI app
- ✅ app/database.py with async setup
- ✅ run.py that starts server
- ✅ GET /api/health endpoint working
- ✅ Swagger UI accessible at /docs
- ✅ Code pushed to GitHub

## 📊 Show Me When Done

1. Screenshot of http://localhost:8000/docs
2. Screenshot of health endpoint response
3. Terminal output: `git log --oneline` (last 3 commits)
4. Terminal output: `python run.py` showing server running

## 🎯 Learning Outcomes

By completing Phase 2:
- ✅ Understanding of configuration management in Python
- ✅ How to create FastAPI apps
- ✅ How to write async endpoints
- ✅ Understanding of app factory pattern
- ✅ How to use FastAPI's auto documentation (Swagger)
- ✅ How to run development server with uvicorn

## ⏱️ Time Estimate: 1-2 hours

Start now! When you have the health endpoint working, show me and we'll move to Phase 3! 🚀
