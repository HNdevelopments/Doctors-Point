git clone <your-repository-url>
cd <repository-name>
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env` file with the following variables:
```
DATABASE_URL=postgresql://username:password@host:port/database
SESSION_SECRET=your-secure-session-secret
MASTER_PASSWORD=your-secure-master-admin-password
```

Make sure to use strong, unique passwords for both SESSION_SECRET and MASTER_PASSWORD.

## Database Migration

1. The database schema is defined in `shared/schema.ts`
2. To migrate the schema to your new database:
```bash
npm run db:push
```

3. If you need to migrate data from the old database:
   - Use pg_dump to export data from the old database
   - Import the data into the new database using psql

## Running the Application

1. Development mode:
```bash
npm run dev
```

2. Production mode:
```bash
npm run build
npm start