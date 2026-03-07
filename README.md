local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

-- Auto Copy Discord Link
setclipboard("https://discord.gg/kejFGz7G5H")

local Window = Rayfield:CreateWindow({
   Name = "Tokra System | Key Verification",
   LoadingTitle = "Checking Access...",
   LoadingStatus = "by Sladostrastnik",
   ConfigurationSaving = {
      Enabled = false
   },
   KeySystem = true,
   KeySettings = {
      Title = "Enter Key",
      Subtitle = "Join Discord for Access",
      Note = "24-Hour Key System (Link Copied!)",
      FileName = "TokraKey",
      SaveKey = false,
      GrabKeyFromSite = false,
      Key = {"E1466%35&227--+dnkfiwooidjfudiiJOGOKLTOKRA73858&77%7@#djciissjsj"}
   }
})

local env = getgenv()
local safeHttpGet = function(...)
    local args = {...}
    local url = ""
    for _, v in ipairs(args) do
        if type(v) == "string" and (v:sub(1,4) == "http" or v:find("://")) then
            url = v
            break
        end
    end
    if url ~= "" then
        return game:HttpGet(url)
    end
end

env.httpget = safeHttpGet
env.HttpGet = safeHttpGet

if setreadonly then setreadonly(env, false) end
env.identifyexecutor = function() return "Krnl" end

loadstring(game:HttpGet("https://raw.githubusercontent.com/sladostrastnik/TokraScript/refs/heads/main/Loader.luau"))()
