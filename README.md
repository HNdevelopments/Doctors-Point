# Backend environment variables
DATABASE_URL=your_postgresql_connection_string
SESSION_SECRET=your_session_secret

# Frontend environment variables
VITE_API_URL=your_backend_api_url
```

## Local Development

1. Clone the repository:
```bash
git clone https://github.com/your-username/doctors-point.git
cd doctors-point
```

2. Install dependencies:
```bash
npm install
```

3. Push the database schema:
```bash
npm run db:push
```

4. Start the development server:
```bash
npm run dev