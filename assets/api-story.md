## NICHE POC API Story


### Purpose
Create a working instance of a dynamic NICHE where STIGS can exist, be dsicovered, collected, and completed by PHERROs.

### Story
Assume a single hypermedia document (the NICHE) that lists one or more STIGs in various states (`waitng`, `working`, `done`). What is the minimum viable working set for an operative NICHE? 

### Data
The NICHE is nothing but a blank document that can host STIGs as identifiable hypermedia controls (elements). There should be some basic metadata about the NICHE (health, population, activity, etc.). 

### Actions
When interacting with a NICHE, other entities (STIGs and PHERROs) should be able to:

 * get a `list` of elements (STIGs & PHERROs) in this NICHE
 * `read` the details of a single STIG
 * change the `status` value of a STIG (`waiting`, `working`, `done`). Can the NICHE do this or just PHERROs?
 * `create` a new STIGs in the NICHE (only a STIG can create another?)
 * `remove` an existing STIG from the NICHE (where does it "go"?)
 * `filter` the view of STIGs and PHERROs in the NICHE
   * show only STIGs or only PHERROs 
   * show only STIGs in certain state (`waiting`)
   * show only PHERROs currently `working` (is this needed?)
   * filter by `dateCreated`, `dateUpdated`, `dateLastTouched`
 * `cull` STIGs and PHERROs from the NICHE (when they are old/dead/inactive)
 * indicate the `status` of the NICHE (see Processing and Rules)
 * return `health` data to anyone asking about this NICHE (???)

### Processing

 * Generate unique `id` values when creating new STIGs.
 * Preserve existing `id` values when adding an existing PHERRO to the NICHE. 
 * Routinely `cull` old STIGs from the NICHE (see Rules)
 * Consider adding a `niche.status` value to indicate health of the NICHE (overcrowding, lack of food/energy, illness?)

### Rules
TK

