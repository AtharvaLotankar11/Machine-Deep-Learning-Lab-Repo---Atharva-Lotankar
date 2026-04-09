# Security Setup Guide

## Environment Variables Required

This project requires several environment variables to run. **NEVER commit actual .env files to git.**

### Backend (.env)
Create `backend/.env` with:
```
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=5432
SECRET_KEY=your-django-secret-key

EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_app_password

RECAPTCHA_SECRET_KEY=your_recaptcha_secret
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
```

### Frontend (.env.local)
Create `frontend/.env.local` with:
```
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

NEXT_PUBLIC_RECAPTCHA_SITE_KEY=your_site_key
NEXT_PUBLIC_RAZORPAY_KEY_ID=your_public_key
```

### Blockchain (.env)
Create `blockchain/.env` with:
```
ALCHEMY_API_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR_API_KEY
PRIVATE_KEY=your_wallet_private_key
```

## Important Security Notes

1. All `.env` files are gitignored
2. Use `.env.example` files as templates
3. Never share private keys or API secrets
4. Rotate all keys if accidentally exposed
5. Use different keys for development and production
