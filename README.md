# match-leads

**User Story**: Match Leads to Agents
As a system,
I want to match leads to state agents based on their profiles and available credits,
So that leads are efficiently distributed to agents who are best suited and have the highest potential for conversion.

### **Acceptance Criteria:**

1. **Lead and State Agent Data:**
   - **Lead Data:**
     - **Region:** (e.g., 'centro')
     - **Property Type:** (e.g., 'casa')
     - **Market Segmentation:** (e.g., 'Minha Casa, Minha Vida')

   - **State Agent Data:**
     - **Credit:** (e.g., 300 credits)
     - **Regions of Interest:** (e.g., ['centro', 'norte'])
     - **Property Types:** (e.g., ['casa', 'apartamento'])
     - **Market Segmentation:** (e.g., ['Minha Casa, Minha Vida', 'Propriedades de alto padrão'])

2. **Matching Criteria:**
   - **Region Match:** The agent’s regions of interest should include the lead's region.
   - **Property Type Match:** The agent’s property types should include the lead's property type.
   - **Market Segmentation Match:** The agent’s market segmentation should include the lead's market segment.

3. **Scoring System:**
   - **Score Calculation:**
     - **Region Match:** Adds 10 points.
     - **Property Type Match:** Adds 20 points.
     - **Market Segmentation Match:** Adds 25 points.

4. **Credit Proportionality:**
   - **Probability of Assignment:** Adjust the probability of assigning a lead to an agent based on their credit proportion relative to the total credit.
   - **Example:** If an agent has 300 credits out of a total of 1000 credits, their probability of receiving a lead is 30% (300/1000).

5. **Lead Assignment:**
   - Assign the lead to the agent with the highest score, adjusted by credit proportionality.

