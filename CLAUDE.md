# Abstract documentation built with Mintlify

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components
- Platform: Documentation for Abstract blockchain - EVM-compatible Layer 2 with native account abstraction

## Documentation structure

### Main sections (tabs in docs.json)
1. **Documentation** - Core Abstract documentation
   - Overview (overview.mdx, what-is-abstract.mdx, connect-to-abstract.mdx)
   - Build on Abstract - Developer guides for smart contracts and applications
   - How Abstract Works - Architecture and technical details
   - Tooling - Block explorers, bridges, faucets, deployed contracts
   - Infrastructure - Node setup and components

2. **Abstract Global Wallet** - Smart contract wallet system
   - Overview and getting started
   - Library Integrations (React hooks, wallet connectors)
   - Abstract Client (core client functionality)
   - Wallet Actions (transaction handling)
   - Session Keys (authentication system)
   - FIAT On-ramp (payment integration)
   - Utils (helper functions)

3. **Ecosystem** - Third-party tools and services
   - automation, bridges, indexers, interoperability, multi-sig-wallets, oracles, paymasters, relayers, rpc-providers, token-distribution

4. **Cookbook** - Code examples and recipes

5. **API Reference** - OpenAPI specification
   - Uses openapi.json for automated API docs

### Key directories
- `/abstract-global-wallet/` - AGW client SDKs and React hooks documentation
- `/build-on-abstract/` - Developer onboarding (Hardhat, Foundry, Ethers, Viem, Thirdweb)
- `/how-abstract-works/` - Technical architecture documentation
- `/ecosystem/` - Third-party integrations
- `/images/` - Documentation assets
- `/snippets/` - Reusable code snippets
- `/api-reference/` - API documentation

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Common patterns in existing content
- Use CardGroup components for organizing related links
- Include code examples with proper language tags
- Use relative paths for internal navigation
- Include both overview pages and detailed implementation guides
- Leverage Mintlify components (Card, CardGroup, Icon) for better UX

## docs.json
- Refer to the [docs.json schema](https://mintlify.com/docs.json) when building the docs.json file and site navigation
- Current theme: "mint" with Abstract branding (green color scheme)
- Has contextual options for copy, chatgpt, claude, mcp, cursor
- Includes redirects for moved content
- Footer includes X, Discord, GitHub social links

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation
- Optional: sidebarTitle (for custom sidebar display)

## Writing standards
- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification