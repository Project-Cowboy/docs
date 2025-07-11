# Getting Started

Welcome to Cowboy — a privacy-preserving protocol that lets you prove facts about web data using zero-knowledge proofs. This guide will walk you through setting up your environment, generating your first proof, and writing your own integration.

---

## 🧰 What You'll Need

Before proving anything, you need two components installed:

- **Cowboy TLSN Browser Extension**  
  Captures web requests and works with a notary server to produce TLS Notary proofs.

- **Cowboy Prover Docker Container**  
  Generates RISC Zero zk-STARK proofs based on your TLS Notary transcript and custom logic.

➡️ See [Resources](./resources.md) for setup instructions.

---

## ✅ Quick Start Steps

1. **Install the Cowboy TLSN Extension**
   - Follow the steps in [Resources](./resources.md).
   - Configure it to use Cowboy’s hosted notary server.

2. **Run the Cowboy Prover Locally**

   ```bash
   docker run -p 1881:1881 --platform linux/amd64 ghcr.io/project-cowboy/cowboy-prover:latest

3. **Capture a Web Request**
Use the extension to browse to a site like x.com, then trigger the notarization flow.

4. **Generate and Submit a Proof**
After capturing the TLS Notary proof, click the On-chain tab in the extension to:
    - Connect to a devnet node
    - Create a wallet and claim test funds
    - Look up any existing integration
    - Prove and submit your data to the network

See the Generating and Submitting Proofs guide for full details.

## 🧪 Test an Example Integration

Want to see what Cowboy can do? Try one of the example integrations:
- X.com account proof
- TikTok influencer tier, without revealing folllower count or username

These use preconfigured endpoints and logic to showcase how custom integrations work.

## 🛠️ Write Your Own Integration

Once you're comfortable submitting proofs, try writing your own:
- Write a Rust program that parses the TLS Notary proof and asserts your desired conditions.
- Use the prover to generate the app-specific zk-STARK proof.
- Upload your integration to the chain and start verifying onchain.

Check out the Developer Examples for structure, utilities, and inspiration.

## Repo
Check out the Repo [here](https://github.com/Project-Cowboy/example-integrations)

## 🧠 Learn More
- [Introduction](./introduction.md): What Cowboy is and why it matters.
- [FAQs](./faqs.md): Get clarity on integrations, proof types, and more.
- [Resources](./resources.md): All tools in one place.