# Certify - Blockchain Certificate Verification Platform

A modern, secure platform for issuing, managing, and verifying certificates using blockchain technology.

## 🚀 Features

- **Issue Certificates**: Create blockchain-verified digital certificates with beautiful PDFs
- **QR Code Generation**: Each certificate includes a QR code for instant verification
- **Blockchain Storage**: Certificate hashes stored on Polygon testnet (Mumbai)
- **Instant Verification**: Verify authenticity in seconds via QR scan or certificate ID
- **Dashboard**: View and manage all issued certificates
- **Tamper-Proof**: Certificates cannot be altered once issued

## 🛠️ Tech Stack

### Frontend
- React 18
- React Router for navigation
- Axios for API calls
- Lucide React for icons
- QRCode.React for QR generation
- Custom CSS for styling

### Backend
- Node.js with Express
- SQLite database
- ethers.js for blockchain interaction
- PDFKit for PDF generation
- QRCode for QR code generation

### Blockchain
- Polygon Mumbai Testnet
- Ethereum-compatible smart contracts

## 📦 Installation

1. **Clone the repository**
   ```bash
   cd Certify
   ```

2. **Install root dependencies**
   ```bash
   npm install
   ```

3. **Install server dependencies**
   ```bash
   cd server
   npm install
   cd ..
   ```

4. **Install client dependencies**
   ```bash
   cd client
   npm install
   cd ..
   ```

5. **Configure environment variables**
   ```bash
   cd server
   cp .env.example .env
   ```
   
   Edit `.env` and add your:
   - Polygon Mumbai RPC URL (or use local Ganache)
   - Private key for blockchain transactions
   - Contract address (after deployment)

## 🚀 Running the Application

### Development Mode (Both servers simultaneously)
```bash
npm run dev
```

This will start:
- Backend server on http://localhost:5000
- Frontend server on http://localhost:3000

### Or run separately:

**Backend only:**
```bash
npm run server
```

**Frontend only:**
```bash
npm run client
```

## 📱 Using the Platform

### Issue a Certificate
1. Navigate to `/issue`
2. Fill in learner details, course name, institute name, and date
3. Click "Issue Certificate"
4. Download the PDF or view the certificate online
5. Share the QR code or certificate ID with the learner

### Verify a Certificate
1. Navigate to `/verify`
2. Enter the certificate ID or scan the QR code
3. View instant verification results from the blockchain

### Dashboard
1. Navigate to `/dashboard`
2. View all issued certificates
3. Search and filter certificates
4. Click "View" to see certificate details

## 🏗️ Project Structure

```
Certify/
├── client/                 # React frontend
│   ├── public/
│   └── src/
│       ├── pages/         # Page components
│       ├── styles/        # CSS files
│       ├── App.js
│       └── index.js
├── server/                # Node.js backend
│   ├── blockchain/        # Blockchain integration
│   ├── database/          # SQLite setup
│   ├── routes/            # API routes
│   ├── utils/             # Utility functions
│   ├── certificates/      # Generated PDFs
│   └── index.js
└── package.json           # Root package file
```

## 🔐 Security Features

- **Blockchain Verification**: All certificates are cryptographically secured
- **Hash Storage**: Only hashes are stored on blockchain, not personal data
- **Tamper Detection**: Any modification is instantly detectable
- **Unique IDs**: Each certificate has a unique identifier

## 🌐 API Endpoints

### Certificates
- `POST /api/certificates/issue` - Issue a new certificate
- `GET /api/certificates/:id` - Get certificate by ID
- `GET /api/certificates` - Get all certificates

### Verification
- `GET /api/verify/:id` - Verify certificate by ID
- `POST /api/verify/hash` - Verify by certificate hash

## 🎨 Design Features

- Clean, modern UI with gradient accents
- Responsive design for mobile and desktop
- Smooth animations and transitions
- Professional certificate layout
- Accessible color scheme

## 🔧 Blockchain Setup (Optional)

For production use with Polygon Mumbai:

1. Get test MATIC from [Mumbai Faucet](https://faucet.polygon.technology/)
2. Deploy the smart contract (contract code available on request)
3. Add contract address to `.env`

For local development:
- Use Ganache for local blockchain
- Update RPC URL in `.env` to `http://127.0.0.1:8545`

## 📄 License

MIT License - feel free to use this project for your needs.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For issues or questions, please open an issue on GitHub.

---

Built with ❤️ using React, Node.js, and Blockchain Technology
