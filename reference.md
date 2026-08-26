# Reference
## gateway
<details><summary><code>client.Gateway.ListModels() -> *dtgsdkgo.ModelList</code></summary>
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

<details><summary><code>client.Gateway.CreateChatCompletion(request) -> *dtgsdkgo.ChatCompletion</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.ChatCompletionRequest{
    Model: "model",
    Messages: []*dtgsdkgo.ChatMessage{
        &dtgsdkgo.ChatMessage{
            Role: dtgsdkgo.ChatMessageRoleSystem,
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

**model:** `string` — ID của agent (UUID) trên gateway `/v1/chat/completions`.
    
</dd>
</dl>

<dl>
<dd>

**messages:** `[]*dtgsdkgo.ChatMessage` 
    
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

**sessionID:** `*string` — Session ID tùy chỉnh phía client (được orchestrator namespace theo user để chống xung đột).
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` — Thread ID con trong session (tùy chỉnh phía client, namespace theo user).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Gateway.CreateChatCompletionByAgentPath(AgentID, request) -> *dtgsdkgo.ChatCompletion</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.WebhookChatCompletionRequest{
    AgentID: "agent_id",
    Messages: []*dtgsdkgo.ChatMessage{
        &dtgsdkgo.ChatMessage{
            Role: dtgsdkgo.ChatMessageRoleSystem,
            Content: "content",
        },
    },
}
client.Gateway.CreateChatCompletionByAgentPath(
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

**agentID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**model:** `*string` — Tuỳ chọn; agent đã xác định bởi path.
    
</dd>
</dl>

<dl>
<dd>

**messages:** `[]*dtgsdkgo.ChatMessage` 
    
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

**sessionID:** `*string` — Session ID tùy chỉnh phía client (được orchestrator namespace theo user để chống xung đột).
    
</dd>
</dl>

<dl>
<dd>

**threadID:** `*string` — Thread ID con trong session (tùy chỉnh phía client, namespace theo user).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## agents
<details><summary><code>client.Agents.ListAgents() -> *dtgsdkgo.ListAgentsResponse</code></summary>
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

<details><summary><code>client.Agents.CreateAgent(request) -> *dtgsdkgo.CreateAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.AgentCreateRequest{
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

<dl>
<dd>

**knowledgeIDs:** `[]string` — UUID các knowledge item gắn agent (điền vào dtg_knowledge_ids).
    
</dd>
</dl>

<dl>
<dd>

**enabledTools:** `[]string` — ID tool từ catalog (dtg_enabled_tools), vd knowledge_rag.
    
</dd>
</dl>

<dl>
<dd>

**mcpDynamicServerIDs:** `[]string` — UUID MCP server động (apimcp) gắn agent.
    
</dd>
</dl>

<dl>
<dd>

**mcpDynamicToolFilter:** `map[string]any` — Filter tool expose cho agent (Dai Agent) theo từng MCP server động (khóa = UUID server).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.GetAgent(ID) -> *dtgsdkgo.GetAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.GetAgentRequest{
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

<details><summary><code>client.Agents.DeleteAgent(ID) -> *dtgsdkgo.DeleteAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.DeleteAgentRequest{
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

<details><summary><code>client.Agents.UpdateAgent(ID, request) -> *dtgsdkgo.UpdateAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.AgentUpdateRequest{
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

<dl>
<dd>

**knowledgeIDs:** `[]string` — Omit/null = giữ nguyên; [] = xoá.
    
</dd>
</dl>

<dl>
<dd>

**enabledTools:** `[]string` — Omit/null = giữ nguyên; [] = xoá.
    
</dd>
</dl>

<dl>
<dd>

**mcpDynamicServerIDs:** `[]string` — Omit/null = giữ nguyên; [] = xoá.
    
</dd>
</dl>

<dl>
<dd>

**mcpDynamicToolFilter:** `map[string]any` — Omit/null = giữ nguyên; {} = xoá.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.StartAgent(ID) -> *dtgsdkgo.StartAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.StartAgentRequest{
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

<details><summary><code>client.Agents.StopAgent(ID) -> *dtgsdkgo.StopAgentResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.StopAgentRequest{
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

<details><summary><code>client.Agents.GetAgentChannels(ID) -> *dtgsdkgo.GetAgentChannelsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.GetAgentChannelsRequest{
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

<details><summary><code>client.Agents.UpdateAgentChannels(ID, request) -> *dtgsdkgo.UpdateAgentChannelsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.UpdateAgentChannelsRequest{
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

**channels:** `[]*dtgsdkgo.ChannelConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Agents.ListAgentModels() -> *dtgsdkgo.ModelList</code></summary>
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
<details><summary><code>client.APIKeys.ListAPIKeys() -> *dtgsdkgo.ListAPIKeysResponse</code></summary>
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

<details><summary><code>client.APIKeys.CreateAPIKey(request) -> *dtgsdkgo.CreateAPIKeyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.APIKeyCreateRequest{
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

<details><summary><code>client.APIKeys.RevokeAPIKey(ID) -> *dtgsdkgo.RevokeAPIKeyResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.RevokeAPIKeyRequest{
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
<details><summary><code>client.Organizations.GetOrganization(ID) -> *dtgsdkgo.GetOrganizationResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.GetOrganizationRequest{
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

<details><summary><code>client.Organizations.ListOrganizationMembers(ID) -> *dtgsdkgo.ListOrganizationMembersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.ListOrganizationMembersRequest{
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
<details><summary><code>client.Knowledge.ListKnowledge() -> *dtgsdkgo.ListKnowledgeResponse</code></summary>
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

<details><summary><code>client.Knowledge.CreateKnowledge(request) -> *dtgsdkgo.CreateKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.KnowledgeCreateRequest{
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

**content:** `string` — Tối đa 4 MiB
    
</dd>
</dl>

<dl>
<dd>

**contentType:** `*dtgsdkgo.KnowledgeCreateRequestContentType` 
    
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

<details><summary><code>client.Knowledge.GetKnowledge(ID) -> *dtgsdkgo.GetKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.GetKnowledgeRequest{
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

<details><summary><code>client.Knowledge.DeleteKnowledge(ID) -> *dtgsdkgo.DeleteKnowledgeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.DeleteKnowledgeRequest{
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
<details><summary><code>client.McpServers.ListMcpServers() -> *dtgsdkgo.ListMcpServersResponse</code></summary>
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

<details><summary><code>client.McpServers.CreateMcpServer(request) -> *dtgsdkgo.CreateMcpServerResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.McpServerCreateRequest{
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

<details><summary><code>client.McpServers.ListMcpServerTools(ID) -> *dtgsdkgo.ListMcpServerToolsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.ListMcpServerToolsRequest{
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

<details><summary><code>client.McpServers.CreateMcpServerTool(ID, request) -> *dtgsdkgo.CreateMcpServerToolResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &dtgsdkgo.McpServerToolCreateRequest{
    ID: "id",
    Kind: dtgsdkgo.McpServerToolCreateRequestKindRest,
    Slug: "slug",
    DisplayName: "display_name",
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

**kind:** `*dtgsdkgo.McpServerToolCreateRequestKind` 
    
</dd>
</dl>

<dl>
<dd>

**slug:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**baseURL:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**restResourcePath:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**authType:** `*dtgsdkgo.McpServerToolCreateRequestAuthType` 
    
</dd>
</dl>

<dl>
<dd>

**authConfig:** `*dtgsdkgo.McpAuthConfig` 
    
</dd>
</dl>

<dl>
<dd>

**endpoints:** `[]*dtgsdkgo.McpEndpoint` 
    
</dd>
</dl>

<dl>
<dd>

**definition:** `*dtgsdkgo.McpToolDefinition` 
    
</dd>
</dl>

<dl>
<dd>

**sortOrder:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**isActive:** `*bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

