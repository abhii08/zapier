for starting the project run the following commands:

1. start the database locally:
docker run --platform linux/amd64 -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword postgres

2. start the primary-backend:
cd primary-backend
npx prisma db seed
npm run dev

3. start the frontend:
cd frontend
npm run dev

4. start the hook:
cd hooks
npm run dev

5. start the kafka locally:
cd processor/kafka-docker
docker compose up

6. start the processor:
cd processor
npm run dev

7. start the worker:
cd worker
npm run dev