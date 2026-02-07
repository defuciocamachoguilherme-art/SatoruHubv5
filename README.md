local Libary = loadstring(game:HttpGet("local redzlib = loadstring(game:HttpGet("https://pastefy.app/JoaoaDi1/raw"))()



local Tab = Window:MakeTab({"tetse", "skull"})
local Tab = Window:MakeTab({"tetse", "skull"})
local Tab = Window:MakeTab({"tetse", "skull"})


game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer(table.unpack({
                [1] = "RolePlayName",
                [2] = "[ Satoru Hub User ]"
                }))
                
                -- Define a bio do jogador
                game:GetService("ReplicatedStorage").RE["1RPNam1eTex1t"]:FireServer(table.unpack({
                    [1] = "RolePlayBio",
                    [2] = "Criador: gui_official_007",
                }))
                
                
local Window = Libary:MakeWindow({
    Title = "Satoru Hub| Brookhaven RP🇧🇷 ",
    SubTitle = "by gui_official",
    LoadText = "Carregando Hub",
    Flags = "Hub_Broookhaven"
})
Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://122623627187728", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

-- =========================================================
-- INFORMAÇÕES E CRÉDITOS - SATORU HUB BROOKHAVEN RP
-- =========================================================

local InfoTab = Window:MakeTab({ "Info", "info" })

-- =========================================================
-- SEÇÃO: INFORMAÇÕES PRINCIPAIS
-- =========================================================
InfoTab:AddSection({ "Informações Principais" })

InfoTab:AddParagraph({ "Nome do Hub:", "Satoru Hub | Brookhaven Rp🏡" })
InfoTab:AddParagraph({ "Desenvolvedores:", " gui_official & black" })
InfoTab:AddParagraph({ "Versão:", "1.0 - Janeiro de 2026" })
InfoTab:AddParagraph({ "Idioma:", "Português (Brasil)" })
InfoTab:AddParagraph({ "Jogo Principal:", "Brookhaven RP 🏡" })
InfoTab:AddParagraph({ "Compatibilidade:", " PC | 📱 Celular | 💊 Tablet" })

-- =========================================================
-- SEÇÃO: CRÉDITOS
-- =========================================================
InfoTab:AddSection({ "Créditos" })

InfoTab:AddParagraph({ "Projeto:", "Satoru Hub © 2026" })
InfoTab:AddParagraph({ "Design e Scripts:", "Gui_official" })
InfoTab:AddParagraph({ "Efeitos e Visual:", "Blackzin & Gui" })
InfoTab:AddParagraph({ "Equipe:", "Satoru Hub Dev Team" })

-- =========================================================
-- SEÇÃO: REDES OFICIAIS
-- =========================================================
InfoTab:AddSection({ "Redes Oficiais" })

InfoTab:AddDiscordInvite({
    Name = "Servidor satoru Hub",
    Description = "Entre na nossa comunidade no Discord 💬",
    Logo = "rbxassetid://122623627187728",
    Invite = "https://discord.gg/mRpVDmUAH"
})

InfoTab:AddDiscordInvite({
    Name = "Gui_official",
    Description = "TikTok Oficial 🎥",
    Logo = "rbxassetid://122623627187728",
    Invite = "https://www.tiktok.com/@gui_official_007?_r=1&_t=ZM-91ImhLXFpEa"
})

-- =========================================================
-- SEÇÃO: INFORMAÇÕES DO JOGADOR
-- =========================================================
InfoTab:AddSection({ "Informações do Jogador" })

local Players = game:GetService("Players")
local Stats = game:GetService("Stats")
local player = Players.LocalPlayer

local function getStatValue(parent, name)
    if parent then
        local obj = parent:FindFirstChild(name)
        if obj and obj.GetValue then
            local sucesso, valor = pcall(function() return obj:GetValue() end)
            if sucesso then
                return math.floor(valor)
            end
        end
    end
    return "Não identificado"
end

local info = {}

info["Usuário:"] = player.Name or "Não identificado"
info["Nome de Exibição:"] = player.DisplayName or "Não identificado"
info["ID do Usuário:"] = player.UserId or "Não identificado"
info["Idade da Conta:"] = player.AccountAge or "Não identificado"

local netStats = Stats:FindFirstChild("Network")
local serverStats = netStats and netStats:FindFirstChild("ServerStatsItem")
info["Ping:"] = (serverStats and getStatValue(serverStats, "Data Ping") .. " ms") or "Não identificado"

if identifyexecutor then
    local sucesso, nome, versao = pcall(function() return identifyexecutor() end)
    info["Executor:"] = sucesso and (nome .. (versao and (" v" .. versao) or "")) or "Não identificado"
else
    info["Executor:"] = "Não identificado"
end

for chave, valor in pairs(info) do
    InfoTab:AddParagraph({ chave, tostring(valor) })
end

InfoTab:AddParagraph({ "Idioma:", "Português" })
InfoTab:AddParagraph({ "Jogo:", "Brookhaven RP 🏡" })
InfoTab:AddParagraph({ "Hub Ativo:", "Satoru Hub" })
InfoTab:AddParagraph({ "Versão do Hub:", "1.0" })

-- =========================================================
-- SEÇÃO: MENSAGENS
-- =========================================================
InfoTab:AddSection({ "Mensagens" })
InfoTab:AddParagraph({ "Mensagem:", "Mostre seu estilo e aproveite o Satoru Hub com classe! " })
InfoTab:AddParagraph({ "Nota:", "Criado para diversão, criatividade e estilo — Satoru Hub BR 💜" })

-- =========================================================
-- SEÇÃO: OUTROS + ANIMAÇÃO VISUAL COM SOM
-- =========================================================
InfoTab:AddSection({ "Outros" })

InfoTab:AddButton({
    Name = "🔁 Reentrar no Servidor",
    Callback = function()
        local TeleportService = game:GetService("TeleportService")
        TeleportService:TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
    end
})

InfoTab:AddButton({
    Name = "💫 Créditos Visuais",
    Callback = function()
        game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Saroru Hub - Créditos ",
            Text = "Feito com estilo por Gui_official & black",
            Duration = 5
        })
    end
})

-- =========================================================
-- ✨ ANIMAÇÃO VISUAL + SOM AO ABRIR A ABA INFO
-- =========================================================
--=========================================================
-- SATORU HUB • PURPLE LOADING SCREEN
--=========================================================

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local RunService = game:GetService("RunService")
local SoundService = game:GetService("SoundService")

local Player = Players.LocalPlayer
if not Player then return end
local PlayerGui = Player:WaitForChild("PlayerGui")

--=========================================================
-- CONFIGURAÇÃO
--=========================================================
local LoadingConfig = {
    Duration = 8,
    FadeOutTime = 1.5,

    BarColor = Color3.fromRGB(138, 43, 226),
    BarGlow  = Color3.fromRGB(186, 85, 211),

    BackgroundColor = Color3.fromRGB(12, 0, 25),
    TextColor = Color3.fromRGB(230, 200, 255),

    ParticleCount = 350,
    ParticleSpeed = 2,
    ParticleSize = 3
}

local LoadingTexts = {
    "Inicializando Satoru Hub...",
    "Carregando módulos...",
    "Aplicando tema roxo...",
    "Preparando interface...",
    "Satoru Hub pronto 😈"
}

--=========================================================
-- SOM
--=========================================================
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://122706595087279"
sound.Volume = 1
sound.Looped = false
sound.Parent = SoundService

--=========================================================
-- PARTICULAS
--=========================================================
local Particles = {}

local function CreateParticle(parent, x, y)
    local p = Instance.new("Frame")
    p.Parent = parent
    p.Size = UDim2.new(0, 3, 0, 3)
    p.Position = UDim2.new(0, x, 0, y)
    p.BorderSizePixel = 0
    p.ZIndex = 8
    p.BackgroundTransparency = math.random(30,70)/100

    Instance.new("UICorner", p).CornerRadius = UDim.new(1,0)

    local g = Instance.new("UIGradient", p)
    g.Color = ColorSequence.new({
        ColorSequenceKeypoint.new(0, Color3.fromRGB(200,160,255)),
        ColorSequenceKeypoint.new(0.5, Color3.fromRGB(138,43,226)),
        ColorSequenceKeypoint.new(1, Color3.fromRGB(230,200,255))
    })

    return {
        frame = p,
        vx = math.random(-2,2),
        vy = math.random(-2,2)
    }
end

local function SpawnParticles(parent)
    local size = workspace.CurrentCamera.ViewportSize
    for i = 1, LoadingConfig.ParticleCount do
        table.insert(Particles,
            CreateParticle(parent,
                math.random(0,size.X),
                math.random(0,size.Y)
            )
        )
    end
end

--=========================================================
-- UI
--=========================================================
local function CreateUI()
    local gui = Instance.new("ScreenGui", PlayerGui)
    gui.IgnoreGuiInset = true
    gui.ResetOnSpawn = false

    local main = Instance.new("Frame", gui)
    main.Size = UDim2.new(1,0,1,0)
    main.BackgroundColor3 = LoadingConfig.BackgroundColor

    local center = Instance.new("Frame", main)
    center.Size = UDim2.new(0,600,0,300)
    center.Position = UDim2.new(0.5,-300,0.5,-150)
    center.BackgroundTransparency = 1

    local title = Instance.new("TextLabel", center)
    title.Size = UDim2.new(1,0,0,80)
    title.BackgroundTransparency = 1
    title.Text = "SATORU HUB"
    title.Font = Enum.Font.GothamBold
    title.TextScaled = true
    title.TextColor3 = LoadingConfig.TextColor

    local tg = Instance.new("UIGradient", title)
    tg.Color = ColorSequence.new({
        ColorSequenceKeypoint.new(0, Color3.fromRGB(186,85,211)),
        ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255,255,255)),
        ColorSequenceKeypoint.new(1, Color3.fromRGB(138,43,226))
    })
    TweenService:Create(
        tg,
        TweenInfo.new(3,Enum.EasingStyle.Sine,Enum.EasingDirection.InOut,-1,true),
        {Offset = Vector2.new(2,0)}
    ):Play()

    local barBg = Instance.new("Frame", center)
    barBg.Size = UDim2.new(1,0,0,25)
    barBg.Position = UDim2.new(0,0,0,120)
    barBg.BackgroundColor3 = Color3.fromRGB(20,20,20)
    Instance.new("UICorner", barBg).CornerRadius = UDim.new(0,12)

    local bar = Instance.new("Frame", barBg)
    bar.Size = UDim2.new(0,0,1,0)
    bar.BackgroundColor3 = LoadingConfig.BarColor
    Instance.new("UICorner", bar).CornerRadius = UDim.new(0,12)

    local bg = Instance.new("UIGradient", bar)
    bg.Color = ColorSequence.new({
        ColorSequenceKeypoint.new(0, LoadingConfig.BarColor),
        ColorSequenceKeypoint.new(0.5, LoadingConfig.BarGlow),
        ColorSequenceKeypoint.new(1, LoadingConfig.BarColor)
    })
    TweenService:Create(
        bg,
        TweenInfo.new(2,Enum.EasingStyle.Sine,Enum.EasingDirection.InOut,-1,true),
        {Offset = Vector2.new(1,0)}
    ):Play()

    local status = Instance.new("TextLabel", center)
    status.Size = UDim2.new(1,0,0,30)
    status.Position = UDim2.new(0,0,0,170)
    status.BackgroundTransparency = 1
    status.TextScaled = true
    status.Font = Enum.Font.Gotham
    status.TextColor3 = Color3.fromRGB(190,170,230)
    status.Text = "Iniciando..."

    return gui, main, bar, status
end

--=========================================================
-- START
--=========================================================
local function StartLoading()
    local gui, main, bar, status = CreateUI()
    SpawnParticles(main)

    sound:Play() -- música começa junto com a tela

    local conn = RunService.Heartbeat:Connect(function()
        local size = workspace.CurrentCamera.ViewportSize
        for _,p in pairs(Particles) do
            p.frame.Position += UDim2.new(0,p.vx,0,p.vy)
            if p.frame.Position.X.Offset > size.X then
                p.frame.Position = UDim2.new(0,0,0,p.frame.Position.Y.Offset)
            end
        end
    end)

    local start = tick()
    local index = 1

    while true do
        local progress = math.clamp((tick()-start)/LoadingConfig.Duration,0,1)
        bar:TweenSize(UDim2.new(progress,0,1,0),"Out","Quad",0.15,true)

        if index <= #LoadingTexts then
            status.Text = LoadingTexts[index]
            index += 1
        end

        if progress >= 1 then break end
        task.wait(0.8)
    end

    TweenService:Create(main, TweenInfo.new(LoadingConfig.FadeOutTime),
        {BackgroundTransparency = 1}):Play()

    TweenService:Create(sound, TweenInfo.new(1), {Volume = 0}):Play()

    task.delay(LoadingConfig.FadeOutTime, function()
        conn:Disconnect()
        sound:Stop()
        gui:Destroy()
    end)
end

task.spawn(StartLoading)


local TrollTab = Window:MakeTab({ Title = "Scripts Trolls", Icon = "rbxassetid://122623627187728" })


TrollTab:AddSection({ "Black Hole" })
TrollTab:AddButton({
    Name = "Black Hole",
    Description = " Ativando isso você puxa Parts até o seu personagem",
    Callback = function()
        local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer
local Workspace = game:GetService("Workspace")

local angle = 1
local radius = 10
local blackHoleActive = false

local function setupPlayer()
    local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

    local Folder = Instance.new("Folder", Workspace)
    local Part = Instance.new("Part", Folder)
    local Attachment1 = Instance.new("Attachment", Part)
    Part.Anchored = true
    Part.CanCollide = false
    Part.Transparency = 1

    return humanoidRootPart, Attachment1
end

local humanoidRootPart, Attachment1 = setupPlayer()

if not getgenv().Network then
    getgenv().Network = {
        BaseParts = {},
        Velocity = Vector3.new(14.46262424, 14.46262424, 14.46262424)
    }

    Network.RetainPart = function(part)
        if typeof(part) == "Instance" and part:IsA("BasePart") and part:IsDescendantOf(Workspace) then
            table.insert(Network.BaseParts, part)
            part.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0)
            part.CanCollide = false
        end
    end

    local function EnablePartControl()
        LocalPlayer.ReplicationFocus = Workspace
        RunService.Heartbeat:Connect(function()
            sethiddenproperty(LocalPlayer, "SimulationRadius", math.huge)
            for _, part in pairs(Network.BaseParts) do
                if part:IsDescendantOf(Workspace) then
                    part.Velocity = Network.Velocity
                end
            end
        end)
    end

    EnablePartControl()
end

local function ForcePart(v)
    if v:IsA("Part") and not v.Anchored and not v.Parent:FindFirstChild("Humanoid") and not v.Parent:FindFirstChild("Head") and v.Name ~= "Handle" then
        for _, x in next, v:GetChildren() do
            if x:IsA("BodyAngularVelocity") or x:IsA("BodyForce") or x:IsA("BodyGyro") or x:IsA("BodyPosition") or x:IsA("BodyThrust") or x:IsA("BodyVelocity") or x:IsA("RocketPropulsion") then
                x:Destroy()
            end
        end
        if v:FindFirstChild("Attachment") then
            v:FindFirstChild("Attachment"):Destroy()
        end
        if v:FindFirstChild("AlignPosition") then
            v:FindFirstChild("AlignPosition"):Destroy()
        end
        if v:FindFirstChild("Torque") then
            v:FindFirstChild("Torque"):Destroy()
        end
        v.CanCollide = false
        
        local Torque = Instance.new("Torque", v)
        Torque.Torque = Vector3.new(1000000, 1000000, 1000000)
        local AlignPosition = Instance.new("AlignPosition", v)
        local Attachment2 = Instance.new("Attachment", v)
        Torque.Attachment0 = Attachment2
        AlignPosition.MaxForce = math.huge
        AlignPosition.MaxVelocity = math.huge
        AlignPosition.Responsiveness = 500
        AlignPosition.Attachment0 = Attachment2
        AlignPosition.Attachment1 = Attachment1
    end
end

local function toggleBlackHole()
    blackHoleActive = not blackHoleActive
    if blackHoleActive then
        for _, v in next, Workspace:GetDescendants() do
            ForcePart(v)
        end

        Workspace.DescendantAdded:Connect(function(v)
            if blackHoleActive then
                ForcePart(v)
            end
        end)

        spawn(function()
            while blackHoleActive and RunService.RenderStepped:Wait() do
                angle = angle + math.rad(2)

                local offsetX = math.cos(angle) * radius
                local offsetZ = math.sin(angle) * radius

                Attachment1.WorldCFrame = humanoidRootPart.CFrame * CFrame.new(offsetX, 0, offsetZ)
            end
        end)
    else
        Attachment1.WorldCFrame = CFrame.new(0, -1000, 0)
    end
end

LocalPlayer.CharacterAdded:Connect(function()
    humanoidRootPart, Attachment1 = setupPlayer()
    if blackHoleActive then
        toggleBlackHole()
    end
end)

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/miroeramaa/TurtleLib/main/TurtleUiLib.lua"))()
local window = library:Window("Projeto LKB")

window:Slider("Radius Blackhole",1,100,10, function(Value)
   radius = Value
end)

window:Toggle("Blackhole", true, function(Value)
       if Value then
            toggleBlackHole()
        else
            blackHoleActive = false
        end
end)

spawn(function()
    while true do
        RunService.RenderStepped:Wait()
        if blackHoleActive then
            angle = angle + math.rad(angleSpeed)
        end
    end
end)

toggleBlackHole()
    end
})


TrollTab:AddSection({ "Puxar Parts" })
TrollTab:AddButton({
    Name = "Puxar Parts",
    Description = "Para usar, chegue perto do Player Selecionado",
    Callback = function()
        -- Gui to Lua
-- Version: 3.2

-- Instances:

local Gui = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local Box = Instance.new("TextBox")
local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
local Label = Instance.new("TextLabel")
local UITextSizeConstraint_2 = Instance.new("UITextSizeConstraint")
local Button = Instance.new("TextButton")
local UITextSizeConstraint_3 = Instance.new("UITextSizeConstraint")

--Properties:

Gui.Name = "Gui"
Gui.Parent = gethui()
Gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = Gui
Main.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.335954279, 0, 0.542361975, 0)
Main.Size = UDim2.new(0.240350261, 0, 0.166880623, 0)
Main.Active = true
Main.Draggable = true

Box.Name = "Box"
Box.Parent = Main
Box.BackgroundColor3 = Color3.fromRGB(95, 95, 95)
Box.BorderColor3 = Color3.fromRGB(0, 0, 0)
Box.BorderSizePixel = 0
Box.Position = UDim2.new(0.0980926454, 0, 0.218712583, 0)
Box.Size = UDim2.new(0.801089942, 0, 0.364963502, 0)
Box.FontFace = Font.new("rbxasset://fonts/families/SourceSansSemibold.json", Enum.FontWeight.Bold, Enum.FontStyle.Normal)
Box.PlaceholderText = "Player here"
Box.Text = ""
Box.TextColor3 = Color3.fromRGB(255, 255, 255)
Box.TextScaled = true
Box.TextSize = 31.000
Box.TextWrapped = true

UITextSizeConstraint.Parent = Box
UITextSizeConstraint.MaxTextSize = 31

Label.Name = "Label"
Label.Parent = Main
Label.BackgroundColor3 = Color3.fromRGB(95, 95, 95)
Label.BorderColor3 = Color3.fromRGB(0, 0, 0)
Label.BorderSizePixel = 0
Label.Size = UDim2.new(1, 0, 0.160583943, 0)
Label.FontFace = Font.new("rbxasset://fonts/families/Nunito.json", Enum.FontWeight.Bold, Enum.FontStyle.Normal)
Label.Text = "Bring Parts | Made by: Lusquinha_067"
Label.TextColor3 = Color3.fromRGB(255, 255, 255)
Label.TextScaled = true
Label.TextSize = 14.000
Label.TextWrapped = true

UITextSizeConstraint_2.Parent = Label
UITextSizeConstraint_2.MaxTextSize = 21

Button.Name = "Button"
Button.Parent = Main
Button.BackgroundColor3 = Color3.fromRGB(95, 95, 95)
Button.BorderColor3 = Color3.fromRGB(0, 0, 0)
Button.Border
