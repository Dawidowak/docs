[View code on GitHub](https://dune.com/docs/data-tables/raw/solana/vote-transactions.md)

# Vote Transactions

The Vote Transactions section of the Dune Docs project focuses on the Solana.vote_transactions table, which contains the full set of vote transactions submitted by validators to vote on a block. This table can be joined with the non-vote transactions table to get a full breakdown of all transactions. The schema of the Solana.vote_transactions table is the same as the main transactions table.

The guide provides a detailed description of each column in the Solana.vote_transactions table, including the column name, column type, and description. Some of the columns include block_slot, which is the block's slot index in the ledger, block_time, which is the estimated time the block was produced, and fee, which is the fee charged for the transaction. The guide also includes examples of queries that can be run on the Solana.vote_transactions table, such as the Solana transactions past 30 days query available on Dune.xyz.

Overall, the Vote Transactions section of the Dune Docs project provides a comprehensive guide to the Solana.vote_transactions table, including its schema and how it can be used to analyze vote transactions submitted by validators. This information is useful for developers and analysts working with Solana.vote_transactions and looking to gain a deeper understanding of its structure and contents.
## Questions: 
 1. What is the purpose of the dune docs app and how does it relate to blockchain technology?
- The app technical guide does not provide information on the purpose of the dune docs app, so a blockchain SQL analyst may need to seek additional documentation or context. 

2. How does the Solana.vote_transactions table differ from the non-vote transactions table mentioned in the guide?
- The guide mentions that the Solana.vote_transactions table contains only vote transactions submitted by validators to vote on a block, while the non-vote transactions table contains a full breakdown of all transactions. A blockchain SQL analyst may want to know more about the schema and contents of the non-vote transactions table.

3. Can the instructions column in the Solana.vote_transactions table be used to track specific actions taken by validators during the voting process?
- The guide mentions that the instructions column contains a list of instructions to execute in order, but it does not provide information on what those instructions may be. A blockchain SQL analyst may want to know if the instructions can be used to track specific actions taken by validators during the voting process.