# DraftCraftV2


Terminology:
  - Tournament: 
  - Player: 
  - Player Ids: 
  - AvailablePlayers: 
  - AvailablePlayers_Ids:
  - TEAM NFT: 
  - Generate TEAM: 
  - Mint TEAM: 
  - POT:
  - TEAM NFT Score:
  - N: Number of winners to distribute the POT to at the end of a tournament.


  
## Needed Functionality:
  NATIVE TOKEN:
   - Used to burn for randomness while Generating TEAM.
   - Used to Mint TEAM, at a lower cost than the cost in stablecoin.
   - Swap for link, and spend link to make random draw.

  GENERATE TEAM:
    - Burn half the native tokens and use other half to get link to generate a random team.  
    - A struct of team members called AvailablePlayers is stored in a nested mapping that maps wallets to a mapping that maps AvailablePlayers_Ids to bool (Owned or not owned). (Prove that a customer owns all palyer Ids in an AvailablePlayers struct).

  TEAM NFT:
    - A subset of AvailablePlayers chosen by the person minting the team from AvailablePlayers.
    - The TEAM NFT Score is calculated using the realworld players performance.
    - TEAM NFTs are ranked by their score.
    
  POT:
    - When minting a TEAM NFT, part (80%) of the cost of minting is put into a communal prize pool called the POT.
    - Once a Tournament is finished, the POT is distributed to the wallets that own each of the N highest scoring TEAM NFTs.
    - The POT is distributed in the style of a poker tournament distribution.  
        That is, the highest ranking TEAM NFT receives 25% of the POT.
        50% of the POT to the top 10% of TEAM NFTs, while the remaining 25% goes to the top 20% of the ranked TEAM NFTs.
        
  SCORE API:
    - An API that get real world data, calculates scores and updates TEAM NFT scores on chain every half hour.
    
    
    
    
    
    
