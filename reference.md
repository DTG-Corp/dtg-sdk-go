# Reference
## gateway
<details><summary><code>client.Gateway.ListModels() -> *dtgagentsdk.ModelList</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Gateway.ListModels(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Gateway.CreateChatCompletion(request) -> *dtgagentsdk.ChatCompletion</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.ChatCompletionRequest{
    Model: "model",
    Messages: []*dtgagentsdk.ChatMessage{
        &dtgagentsdk.ChatMessage{
            Role: dtgagentsdk.ChatMessageRoleSystem,
            Content: "content",
        },
    },
}
client.Gateway.CreateChatCompletion(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hermesSessionID:** `*string` — Session tùy chỉnh phía client.
    
</dd>
</dl>

<dl>
<dd>

**hermesThreadID:** `*string` — Thread tùy chỉnh phía client.
    
</dd>
</dl>

<dl>
<dd>

**model:** `string` — ID của agent (UUID).
    
</dd>
</dl>

<dl>
<dd>

**messages:** `[]*dtgagentsdk.ChatMessage` 
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` 
    
</dd>
</dl>

<dl>
<dd>

**stream:** `*bool` 
    
</dd>
</dl>

<dl>
<dd>

**sessionID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## agents
<details><summary><code>client.Agents.ListAgents() -> *dtgagentsdk.ListAgentsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Agents.ListAgents(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.CreateAgent(request) -> *dtgagentsdk.CreateAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.AgentCreateRequest{
    DisplayName: "display_name",
}
client.Agents.CreateAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**llmProvider:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmModel:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmBaseURL:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmAPIKey:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.GetAgent(ID) -> *dtgagentsdk.GetAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.GetAgentRequest{
    ID: "id",
}
client.Agents.GetAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.DeleteAgent(ID) -> *dtgagentsdk.DeleteAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.DeleteAgentRequest{
    ID: "id",
}
client.Agents.DeleteAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.UpdateAgent(ID, request) -> *dtgagentsdk.UpdateAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.AgentUpdateRequest{
    ID: "id",
}
client.Agents.UpdateAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmProvider:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmModel:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmBaseURL:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**llmAPIKey:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.StartAgent(ID) -> *dtgagentsdk.StartAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.StartAgentRequest{
    ID: "id",
}
client.Agents.StartAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.StopAgent(ID) -> *dtgagentsdk.StopAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.StopAgentRequest{
    ID: "id",
}
client.Agents.StopAgent(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.GetAgentChannels(ID) -> *dtgagentsdk.GetAgentChannelsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.GetAgentChannelsRequest{
    ID: "id",
}
client.Agents.GetAgentChannels(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.UpdateAgentChannels(ID, request) -> *dtgagentsdk.UpdateAgentChannelsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.UpdateAgentChannelsRequest{
    ID: "id",
}
client.Agents.UpdateAgentChannels(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**channels:** `[]*dtgagentsdk.ChannelConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.ListAgentModels() -> *dtgagentsdk.ModelList</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Agents.ListAgentModels(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## api-keys
<details><summary><code>client.APIKeys.ListAPIKeys() -> *dtgagentsdk.ListAPIKeysResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.APIKeys.ListAPIKeys(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.APIKeys.CreateAPIKey(request) -> *dtgagentsdk.CreateAPIKeyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.APIKeyCreateRequest{
    Name: "name",
}
client.APIKeys.CreateAPIKey(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.APIKeys.RevokeAPIKey(ID) -> *dtgagentsdk.RevokeAPIKeyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.RevokeAPIKeyRequest{
    ID: "id",
}
client.APIKeys.RevokeAPIKey(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## organizations
<details><summary><code>client.Organizations.GetOrganization(ID) -> *dtgagentsdk.GetOrganizationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.GetOrganizationRequest{
    ID: "id",
}
client.Organizations.GetOrganization(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Organizations.ListOrganizationMembers(ID) -> *dtgagentsdk.ListOrganizationMembersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.ListOrganizationMembersRequest{
    ID: "id",
}
client.Organizations.ListOrganizationMembers(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## knowledge
<details><summary><code>client.Knowledge.ListKnowledge() -> *dtgagentsdk.ListKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Knowledge.ListKnowledge(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Knowledge.CreateKnowledge(request) -> *dtgagentsdk.CreateKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.KnowledgeCreateRequest{
    Title: "title",
    Content: "content",
}
client.Knowledge.CreateKnowledge(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**title:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**content:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**contentType:** `*dtgagentsdk.KnowledgeCreateRequestContentType` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Knowledge.GetKnowledge(ID) -> *dtgagentsdk.GetKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.GetKnowledgeRequest{
    ID: "id",
}
client.Knowledge.GetKnowledge(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Knowledge.DeleteKnowledge(ID) -> *dtgagentsdk.DeleteKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.DeleteKnowledgeRequest{
    ID: "id",
}
client.Knowledge.DeleteKnowledge(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## mcp-servers
<details><summary><code>client.McpServers.ListMcpServers() -> *dtgagentsdk.ListMcpServersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.McpServers.ListMcpServers(
    context.TODO(),
)
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.McpServers.CreateMcpServer(request) -> *dtgagentsdk.CreateMcpServerResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.McpServerCreateRequest{
    Name: "name",
}
client.McpServers.CreateMcpServer(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.McpServers.ListMcpServerTools(ID) -> *dtgagentsdk.ListMcpServerToolsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.ListMcpServerToolsRequest{
    ID: "id",
}
client.McpServers.ListMcpServerTools(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.McpServers.CreateMcpServerTool(ID, request) -> *dtgagentsdk.CreateMcpServerToolResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgagentsdk.CreateMcpServerToolRequest{
    ID: "id",
    Body: &dtgagentsdk.McpServerTool{},
}
client.McpServers.CreateMcpServerTool(
    context.TODO(),
    request,
)
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**idempotencyKey:** `*string` — Idempotency key cho mutation (tránh double-submit).
    
</dd>
</dl>

<dl>
<dd>

**request:** `*dtgagentsdk.McpServerTool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

