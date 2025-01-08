Revised Rarities:
Common
Rare
Ultra Rare
Secret Rare
Mosaic Rare
Shatterfoil Rare
Rainbow Rare
Updated Plan for Reimagine-Truth-NFT-SAMPLE Repository
1. Repository Structure Overview
We’ll update the repository structure to include only the specified rarities without the Legendary rarity.

plaintext
Copy code
Reimagine-Truth-NFT-SAMPLE/
├── contracts/               # Smart contracts for NFTs and Token
│   ├── ReimagineToken.sol   # ERC-20 token contract for $RTO
│   ├── TruthSeekersNFT.sol  # ERC-721 contract for the NFT collection (with updated rarities)
│   ├── Staking.sol          # Staking contract for $RTO rewards
│   ├── VRMuseum.sol         # Smart contract for VR museum operations
│
├── frontend/                # Frontend code for the marketplace and wallet
│   ├── public/              # Static assets (images, icons, etc.)
│   ├── src/                 # Main frontend source files
│   │   ├── components/      # UI components (e.g., NFT Cards)
│   │   ├── pages/           # Pages for the marketplace and NFTs
│   │   ├── styles/          # CSS for the frontend
│   │   └── App.js           # Entry point for the frontend app
│   └── package.json         # Frontend dependencies
│
├── nft-assets/              # Digital assets for the NFT collection
│   ├── metadata/            # Metadata files for NFTs (updated with new rarities)
│   ├── images/              # High-quality images of NFTs
│   ├── previews/            # Low-res previews for display
│   └── README.md            # Notes on asset management
│
├── docs/                    # Documentation files
│   ├── whitepaper.pdf       # Updated whitepaper
│   ├── tokenomics.md        # $RTO tokenomics
│   ├── technical-architecture.md # Architecture and workflows (including VR)
│   ├── contributing.md      # Guidelines for contributing to the project
│   ├── roadmap.md           # Updated roadmap to include new features
│   └── nft-rarities.md      # Explanation of NFT rarities, types, and benefits
│
├── database/                # Database for storing NFT metadata
│   ├── migrations/          # Migration scripts
│   ├── seeders/             # Seed data for NFTs
│   ├── schema.sql           # Database schema (updated with new attributes)
│   └── card-database.json   # Updated Dueling Nexus format (NFT data)
│
├── tests/                   # Tests for contracts and backend
│   ├── contracts/           # Contract testing scripts (including new rarity logic)
│   ├── backend/             # Backend testing scripts
│   └── README.md            # Testing instructions
│
├── scripts/                 # Utility scripts for deployment and airdrops
│   ├── deploy.js            # Deployment script for smart contracts
│   ├── airdrop.js           # Script for managing airdrops
│   ├── referral-tracking.js # Referral tracking script
│   └── nft-mint.js          # Script for minting NFTs with new rarities
│
├── .env                     # Environment variables
├── .gitignore               # Git ignore rules
├── README.md                # Updated project overview and repository
└── LICENSE                  # License for the project
2. Key Updates to Implement:
A. Smart Contracts Update
TruthSeekersNFT.sol:
Update the ERC-721 contract to handle the seven rarities (Common, Rare, Ultra Rare, Secret Rare, Mosaic Rare, Shatterfoil Rare, Rainbow Rare).
Add the ability to mint NFTs with different rarities and their respective prices.
Remove the Legendary rarity, as it is no longer in use.
Ensure that the contract supports additional attributes such as Level, Attack, Defense, Effect, and Style Variant.
B. NFT Metadata Changes
Update NFT metadata files to include:
Rarity: Common, Rare, Ultra Rare, Secret Rare, Mosaic Rare, Shatterfoil Rare, and Rainbow Rare.
Type: Normal, Effect, Ritual, etc.
Attributes: Power, Style Variant, Level, Attack, Defense, Effect.
Example for a Common card:
json
Copy code
{
  "name": "Truth Seeker #1",
  "description": "A unique NFT from the Truth Seekers Deck collection.",
  "image": "https://ipfs.io/ipfs/QmExampleHash",
  "attributes": [
    { "trait_type": "Rarity", "value": "Common" },
    { "trait_type": "Power", "value": "10" },
    { "trait_type": "Style Variant", "value": "Normal" },
    { "trait_type": "Level", "value": "1" },
    { "trait_type": "Attack", "value": "100" },
    { "trait_type": "Defense", "value": "50" },
    { "trait_type": "Effect", "value": "Basic Truth Seeker" },
    { "trait_type": "Type", "value": "Normal" }
  ]
}
C. Frontend Update
UI for NFT Cards:
Display NFTs with the updated rarities, including all relevant attributes (Rarity, Level, Attack, Defense, Effect, etc.).
Implement sorting and filtering by rarity to make it easier for users to browse NFTs based on their rarity.
D. Database Update
Card Database (card-database.json):
Add all NFTs and their metadata in line with the newly updated rarities.
Example for a Rare NFT:
json
Copy code
{
  "name": "Truth Seeker #2",
  "description": "A Rare NFT with enhanced attributes.",
  "image": "https://ipfs.io/ipfs/QmExampleHash2",
  "attributes": [
    { "trait_type": "Rarity", "value": "Rare" },
    { "trait_type": "Power", "value": "25" },
    { "trait_type": "Style Variant", "value": "Normal" },
    { "trait_type": "Level", "value": "2" },
    { "trait_type": "Attack", "value": "200" },
    { "trait_type": "Defense", "value": "150" },
    { "trait_type": "Effect", "value": "Special power boost" },
    { "trait_type": "Type", "value": "Normal" }
  ]
}
E. Add NFT Rarity Explanation
Updated Document: The nft-rarities.md file will explain the 7 rarities:
Common: Standard cards
Rare: Enhanced attributes
Ultra Rare: High-quality with additional power
Secret Rare: Rare with secret abilities
Mosaic Rare: Unique design
Shatterfoil Rare: Shiny broken effect
Rainbow Rare: Special effects and extreme rarity
F. Tokenomics Update
Ensure that the $RTO token interacts with the NFTs:
$RTO can be used for purchasing NFTs or staking to earn exclusive rewards.
Update minting and pricing logic to incorporate $RTO for NFT purchases and staking.
3. Next Steps for Updating the Repository
A. Update Smart Contract Logic
Add the updated rarity logic to the TruthSeekersNFT.sol contract.
Deploy the updated contract to your chosen blockchain (Optimism, Ethereum, etc.).
B. Update Frontend UI
Make sure the UI reflects the new rarity categories.
Add filtering and sorting options for the rarity types.
C. Update Documentation
Update the README.md with the new rarity structure and token integration.
Add nft-rarities.md to explain the different rarity types and their effects.
