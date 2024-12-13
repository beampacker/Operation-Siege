local v_u_1 = game:GetService("UserInputService")
local v_u_2 = game:GetService("ContextActionService")
local v_u_3 = game:GetService("RunService")
local v_u_4 = game:GetService("TweenService")
local v_u_5 = game:GetService("Debris")
game:GetService("PhysicsService")
local v_u_6 = game:GetService("ReplicatedStorage")
local v7 = game:GetService("Players")
local v_u_8 = game:GetService("CollectionService")
local v_u_9 = workspace:WaitForChild("SE_Workspace")
local v10 = v_u_6:WaitForChild("Skorpio_Engine")
local v_u_11 = v10:WaitForChild("Events")
local v12 = v10:WaitForChild("Modules")
local v_u_13 = v10:WaitForChild("ArmModel")
local v_u_14 = v10:WaitForChild("GunModels")
local v_u_15 = v10:WaitForChild("AttModels")
local v_u_16 = v10:WaitForChild("AttModules")
local v17 = v10:WaitForChild("GameRules")
local v_u_18 = v10:WaitForChild("FX")
local v_u_19 = v_u_6:WaitForChild("Game")
local v_u_20 = v_u_19:WaitForChild("Classes")
local v21 = v_u_19:WaitForChild("Eventos")
local v_u_22 = v7.LocalPlayer
local v_u_23 = v_u_22.Character or v_u_22.CharacterAdded:Wait()
v_u_22:GetMouse()
local v_u_24 = workspace.CurrentCamera
require(v17:WaitForChild("Config"))
local v25 = require(v12:WaitForChild("Spring"))
local v26 = require(v12:WaitForChild("SpringModule"))
local v_u_27 = require(v12:WaitForChild("Hitmarker"))
require(v12:WaitForChild("DebrisModule"))
local v_u_28 = require(v12:WaitForChild("Thread"))
local v_u_29 = require(v12:WaitForChild("Utilities"))
local v_u_30 = require(v12:WaitForChild("DroneModule"))
local v_u_31 = require(v12:WaitForChild("SkinHandler"))
local v_u_32 = 0
local v_u_33 = 0
local v_u_34 = ""
local v_u_35 = ""
local v_u_36 = ""
local v_u_37 = ""
local v_u_38 = 0
local v_u_39 = 0
local v_u_40 = nil
local v_u_41 = nil
local v_u_42 = nil
local v_u_43 = nil
local v_u_44 = nil
local v_u_45 = nil
local v_u_46 = nil
local v_u_47 = nil
local v_u_48 = nil
local v_u_49 = nil
local v_u_50 = nil
local v_u_51 = nil
local v_u_52 = nil
local v_u_53 = nil
local v_u_54 = 1
local v_u_55 = nil
local v_u_56 = nil
local v_u_57 = os.clock()
local v_u_58 = v_u_11.AcessId:InvokeServer(v_u_22.UserId)
local v_u_59 = v21.GetPlayerData:InvokeServer() or {}
local v_u_60
if v_u_59.FOV then
    local v61 = 60 + v_u_59.FOV * 20
    v_u_60 = math.floor(v61) or 70
else
    v_u_60 = 70
end
local v_u_62
if v_u_59.MouseSens then
    local v63 = v_u_59.MouseSens
    v_u_62 = math.clamp(v63, 0.004, 4) or 1
else
    v_u_62 = 1
end
local v_u_64
if v_u_59.ADSSens then
    local v65 = v_u_59.ADSSens
    v_u_64 = math.clamp(v65, 0.004, 4) or 0.5
else
    v_u_64 = 0.5
end
local v_u_66
if v_u_59.ViewmodelFOV then
    local v67 = v_u_59.ViewmodelFOV
    v_u_66 = math.clamp(v67, 0, 1) or 1
else
    v_u_66 = 1
end
local v_u_68 = UDim2.new()
local v_u_69 = UDim2.new()
local v_u_70 = UDim2.new()
local v_u_71 = UDim2.new()
local v_u_72 = 0
local v_u_73 = false
local v_u_74 = false
local v_u_75 = false
local v_u_76 = false
local v_u_77 = false
local v_u_78 = false
local v_u_79 = true
local v_u_80 = false
local v_u_81 = false
local v_u_82 = false
local v_u_83 = false
local v_u_84 = false
local v_u_85 = 1
local v_u_86 = nil
local v_u_87 = nil
local v_u_88 = false
local v_u_89 = false
local v_u_90 = nil
local v_u_91 = nil
local v_u_92 = false
local v_u_93 = 0
local v_u_94 = nil
local v_u_95 = false
local v_u_96 = false
local v_u_97 = CFrame.new()
local v_u_98 = Vector2.new(0, 0)
local v_u_99 = Vector2.new(0, 0)
CFrame.new()
local v_u_100 = CFrame.new()
local v_u_101 = {}
local v_u_102 = 0
local v_u_103 = 0
local v_u_104 = {
    ["camRecoilMod"] = {
        ["RecoilTilt"] = 1,
        ["RecoilUp"] = 1,
        ["RecoilLeft"] = 1,
        ["RecoilRight"] = 1
    },
    ["gunRecoilMod"] = {
        ["RecoilUp"] = 1,
        ["RecoilTilt"] = 1,
        ["RecoilLeft"] = 1,
        ["RecoilRight"] = 1
    },
    ["ZoomValue"] = 60,
    ["AimRM"] = 1,
    ["SpreadRM"] = 1,
    ["DamageMod"] = 1,
    ["minDamageMod"] = 1,
    ["MinRecoilPower"] = 1,
    ["MaxRecoilPower"] = 1,
    ["RecoilPowerStepAmount"] = 1,
    ["MinSpread"] = 1,
    ["MaxSpread"] = 1,
    ["AimInaccuracyStepAmount"] = 1,
    ["AimInaccuracyDecrease"] = 1,
    ["WalkMult"] = 1,
    ["adsTime"] = 1,
    ["MuzzleVelocity"] = 1
}
local v_u_105 = CFrame.new()
local v_u_106 = CFrame.new()
local v_u_107 = CFrame.new()
local v_u_108 = CFrame.new()
local v_u_109 = CFrame.new(0, 0, -0.5)
local v_u_110 = CFrame.new()
local v_u_111 = CFrame.new()
local v_u_112 = CFrame.new()
local v_u_113 = TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.Out, 0, false, 0)
local v_u_114 = {
    v_u_24,
    v_u_23,
    v_u_9.Client,
    v_u_9.Server,
    workspace.MapShadow,
    workspace.DoorHitbox,
    workspace.WallHitbox
}
local v_u_115 = {
    v_u_24,
    v_u_23,
    v_u_9.Client,
    v_u_9.Server,
    workspace.MapShadow,
    workspace.DoorHitbox,
    workspace.WallHitbox
}
function RAND(p116, p117, p118)
    local v119 = 1 / (p118 or 1)
    return math.random(p116 * v119, p117 * v119) / v119
end
v_u_1.MouseDeltaSensitivity = v_u_62
v_u_24.FieldOfView = v_u_60
local v_u_120 = v_u_22.PlayerGui:WaitForChild("SE_GUI")
local v121 = v_u_4:Create(v_u_120.Efeitos.Health, TweenInfo.new(1, Enum.EasingStyle.Circular, Enum.EasingDirection.InOut, -1, true), {
    ["Size"] = UDim2.new(1.2, 0, 1.4, 0)
})
local v122 = v_u_4:Create(v_u_120.Efeitos.LowHealth, TweenInfo.new(1, Enum.EasingStyle.Circular, Enum.EasingDirection.InOut, -1, true), {
    ["Size"] = UDim2.new(1.2, 0, 1.4, 0)
})
local v_u_123 = v_u_120.Crosshair
local v_u_124 = v26.create()
local v_u_125 = v26.create()
local v_u_126 = v26.create()
local v_u_127 = {
    ["cornerPeek"] = v25.new(0)
}
v_u_127.cornerPeek.d = 1
v_u_127.cornerPeek.s = 15
v_u_127.peekFactor = -0.2617993877991494
v_u_127.dirPeek = 0
local v_u_128 = v_u_11.Stance
local v_u_129 = 0
local v_u_130 = 0
local v_u_131 = 0
local v_u_132 = 0
local v_u_133 = v_u_131
local v_u_134 = false
local v_u_135 = false
local v_u_136 = false
local v_u_137 = false
local v_u_138 = true
local v_u_139 = v_u_23:WaitForChild("Humanoid")
local v_u_140 = v_u_139:WaitForChild("Animator")
local v141 = v_u_23:WaitForChild("Head")
v_u_23:WaitForChild("UpperTorso")
local v_u_142 = v_u_23:WaitForChild("HumanoidRootPart")
v_u_23.LowerTorso:WaitForChild("Root")
local v143 = v141:WaitForChild("Neck")
v_u_23.RightUpperArm:WaitForChild("RightShoulder")
v_u_23.LeftUpperArm:WaitForChild("LeftShoulder")
v_u_23.RightUpperLeg:WaitForChild("RightHip")
v_u_23.LeftUpperLeg:WaitForChild("LeftHip")
v_u_139:SetStateEnabled(Enum.HumanoidStateType.FallingDown, false)
local _ = v143.C0
local _ = CFrame.new
local _ = CFrame.Angles
local _ = math.asin
v_u_24:ClearAllChildren()
v_u_9.Client:ClearAllChildren()
v_u_9.Server:ClearAllChildren()
local v_u_144 = false
function HeadMovement()
    -- upvalues: (copy) v_u_22, (copy) v_u_24, (ref) v_u_144, (copy) v_u_30, (ref) v_u_84, (copy) v_u_11
    if v_u_22.Character then
        if v_u_22.Character.PrimaryPart and (v_u_22.Character:FindFirstChild("Humanoid") and v_u_22.Character.Humanoid.Health > 0) then
            if v_u_22.Character.Humanoid.RigType == Enum.HumanoidRigType.R15 then
                local v145 = v_u_22.Character:FindFirstChild("Head")
                if v145 then
                    v145 = v_u_22.Character.Head:FindFirstChild("Neck")
                end
                local v146 = v_u_22.Character:FindFirstChild("RightUpperArm")
                if v146 then
                    v146 = v_u_22.Character.RightUpperArm:FindFirstChild("RightShoulder")
                end
                local v147 = v_u_22.Character:FindFirstChild("LeftUpperArm")
                if v147 then
                    v147 = v_u_22.Character.LeftUpperArm:FindFirstChild("LeftShoulder")
                end
                local v148 = v_u_22.Character:FindFirstChild("UpperTorso")
                if v148 then
                    v148 = v_u_22.Character.UpperTorso:FindFirstChild("Waist")
                end
                local _ = v_u_22.Character.UpperTorso.CFrame:toObjectSpace(v_u_24.CFrame).lookVector
                if v145 and (v146 and v147) then
                    v_u_144 = not v_u_144
                    local v149 = v145.C1
                    local v150 = CFrame.Angles
                    local v151 = v_u_24.CFrame.LookVector.y * 0.8
                    local v152 = -math.asin(v151)
                    local v153 = v_u_22.Character.UpperTorso.CFrame.lookVector.Y
                    local v154 = v149 * v150(v152 + math.asin(v153), 0, 0)
                    local v155 = v148.C1
                    local v156 = CFrame.Angles
                    local v157 = v_u_24.CFrame.LookVector.y * 0.3
                    local v158 = v155 * v156(-math.asin(v157), 0, 0)
                    local v159 = v146.C0
                    local v160 = CFrame.Angles
                    local v161 = -v_u_24.CFrame.LookVector.y * 0.8
                    local v162 = -math.asin(v161)
                    local v163 = v_u_22.Character.UpperTorso.CFrame.lookVector.Y
                    local v164 = v159 * v160(v162 - math.asin(v163), 0, 0)
                    local v165 = v147.C0
                    local v166 = CFrame.Angles
                    local v167 = -v_u_24.CFrame.LookVector.y * 0.8
                    local v168 = -math.asin(v167)
                    local v169 = v_u_22.Character.UpperTorso.CFrame.lookVector.Y
                    local v170 = v165 * v166(v168 - math.asin(v169), 0, 0)
                    if v_u_144 and not (v_u_30.InDrone or v_u_84) then
                        v_u_11.HeadRot:FireServer(v154, v164, v170, v158)
                    end
                end
            end
        else
            return
        end
    else
        return
    end
end
local function v_u_188(p171)
    -- upvalues: (ref) v_u_74, (ref) v_u_48, (ref) v_u_49, (ref) v_u_100, (ref) v_u_72
    if v_u_74 and (v_u_48 and (v_u_48.CanRun and not v_u_49)) then
        local v172 = v_u_100
        local v173 = CFrame.new
        local v174 = 0.00001 * (v_u_72 / 10)
        local v175 = os.clock() * 8
        local v176 = v174 * math.sin(v175)
        local v177 = 0.00001 * (v_u_72 / 10)
        local v178 = os.clock() * 16
        local v179 = v173(v176, v177 * math.cos(v178), 0)
        local v180 = CFrame.Angles
        local v181 = 0.05 * (v_u_72 / 10)
        local v182 = os.clock() * 16
        local v183 = v181 * math.sin(v182)
        local v184 = math.rad(v183)
        local v185 = 0.05 * (v_u_72 / 10)
        local v186 = os.clock() * 8
        local v187 = v185 * math.cos(v186)
        v_u_100 = v172:Lerp(v179 * v180(v184, math.rad(v187), 0), p171)
    else
        v_u_100 = v_u_100:Lerp(CFrame.new(), p171)
    end
end
local function v_u_193(p189)
    -- upvalues: (copy) v_u_127, (ref) v_u_130, (copy) v_u_125, (copy) v_u_24, (ref) v_u_100
    v_u_127.cornerPeek.t = v_u_127.peekFactor * v_u_130
    local v190 = CFrame.fromAxisAngle(Vector3.new(0, 0, 1), v_u_127.cornerPeek.p)
    local v191 = v_u_125:update(p189)
    local v192 = p189 * 20
    v_u_24.CFrame = v_u_24.CFrame * v190 * v_u_100 * CFrame.Angles(v191.X * v192, v191.Y * v192, v191.Z * v192)
end
function InitializeCamera()
    -- upvalues: (copy) v_u_3, (copy) v_u_9, (ref) v_u_130, (ref) v_u_131, (copy) v_u_22, (ref) v_u_120, (ref) v_u_85, (copy) v_u_24, (ref) v_u_97, (copy) v_u_4, (copy) v_u_2
    v_u_3:UnbindFromRenderStep("CamConnection")
    local v_u_194 = {}
    for _, v195 in pairs(v_u_9.Cameras:GetChildren()) do
        if v195:FindFirstChild("Humanoid") and v195.Humanoid.Health > 0 then
            table.insert(v_u_194, v195)
        end
    end
    v_u_130 = 0
    v_u_131 = 0
    Lean()
    local function v_u_202(_)
        -- upvalues: (ref) v_u_22, (ref) v_u_120, (copy) v_u_194, (ref) v_u_85
        if v_u_22.Character then
            local v196 = v_u_120.CameraOverlay.PrankCall.Fox
            local v197 = UDim2.new
            local v198 = os.clock() * 5
            v196.Position = v197(0.5, 0, 0.5, math.sin(v198) * 20)
            v_u_120.CameraOverlay.PrankCall.Visible = v_u_22:FindFirstChild("Prank Call Tag")
            v_u_120.CameraOverlay.Haha.Playing = v_u_22:FindFirstChild("Prank Call Tag")
            v_u_120.CameraOverlay.PrankCall.TileSize = UDim2.new(math.random(400, 750) / 450, 0, math.random(400, 750) / 450, 0)
            if v_u_194[v_u_85] and (v_u_194[v_u_85]:FindFirstChild("Humanoid") and v_u_194[v_u_85].Humanoid.Health > 0) then
                if v_u_194[v_u_85]:FindFirstChild("LocationName") then
                    v_u_120.CameraOverlay.CamName.TextLabel.Text = v_u_194[v_u_85].LocationName.Value
                end
                local v199 = v_u_120.CameraOverlay.WN
                local v200 = math.noise(0.125) * tick()
                local v201 = math.sin(v200) / 4
                v199.ImageTransparency = 0.85 - math.abs(v201)
                v_u_120.CameraOverlay.WN.TileSize = UDim2.new(math.random(400, 600) / 750, 0, math.random(400, 600) / 750, 0)
            else
                v_u_120.CameraOverlay.WN.ImageTransparency = 0
                v_u_120.CameraOverlay.WN.TileSize = UDim2.new(math.random(400, 600) / 750, 0, math.random(400, 600) / 750, 0)
            end
        else
            v_u_120.CameraOverlay.WN.ImageTransparency = 0
            v_u_120.CameraOverlay.WN.TileSize = UDim2.new(math.random(400, 600) / 750, 0, math.random(400, 600) / 750, 0)
            return
        end
    end
    local function v209(p203, p204, _)
        -- upvalues: (ref) v_u_9, (ref) v_u_3, (ref) v_u_85, (ref) v_u_120, (ref) v_u_22, (ref) v_u_24, (copy) v_u_202
        local v205 = {}
        for _, v206 in pairs(v_u_9.Cameras:GetChildren()) do
            if v206:FindFirstChild("Humanoid") and v206.Humanoid.Health > 0 then
                table.insert(v205, v206)
            end
        end
        if p203 == "NextRight" and p204 == Enum.UserInputState.Begin then
            v_u_3:UnbindFromRenderStep("CamConnection")
            while true do
                if v_u_85 + 1 > #v205 then
                    v_u_85 = 1
                    break
                end
                v_u_85 = v_u_85 + 1
                if v205[v_u_85] and v205[v_u_85].Humanoid.Health > 0 then
                    break
                end
            end
            local v207 = v_u_120.CameraOverlay.CamUp:Clone()
            v207.Parent = v_u_22.PlayerGui
            v207.PlayOnRemove = true
            v207:Destroy()
            v205[v_u_85].Humanoid.CameraOffset = v205[v_u_85]:GetAttribute("CamOffset") or Vector3.new(0, 0, 0)
            v_u_24.CameraSubject = v205[v_u_85]
            v_u_24.CFrame = v205[v_u_85].PrimaryPart.CFrame
            v_u_24.CameraType = Enum.CameraType.Custom
            v_u_24.FieldOfView = 50
            v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
            v_u_3:BindToRenderStep("CamConnection", Enum.RenderPriority.Last.Value, v_u_202)
        elseif p203 == "PrevCam" and p204 == Enum.UserInputState.Begin then
            v_u_3:UnbindFromRenderStep("CamConnection")
            while true do
                if v_u_85 - 1 < 1 then
                    v_u_85 = #v205
                    break
                end
                v_u_85 = v_u_85 - 1
                if v205[v_u_85] and v205[v_u_85].Humanoid.Health > 0 then
                    break
                end
            end
            local v208 = v_u_120.CameraOverlay.CamDown:Clone()
            v208.Parent = v_u_22.PlayerGui
            v208.PlayOnRemove = true
            v208:Destroy()
            v205[v_u_85].Humanoid.CameraOffset = v205[v_u_85]:GetAttribute("CamOffset") or Vector3.new(0, 0, 0)
            v_u_24.CameraSubject = v205[v_u_85]
            v_u_24.CFrame = v205[v_u_85].PrimaryPart.CFrame
            v_u_24.CameraType = Enum.CameraType.Custom
            v_u_24.FieldOfView = 50
            v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
            v_u_3:BindToRenderStep("CamConnection", Enum.RenderPriority.Last.Value, v_u_202)
        end
    end
    if v_u_194[v_u_85] and v_u_194[v_u_85].Humanoid.Health > 0 then
        v_u_97 = v_u_24.CFrame
        v_u_4:Create(v_u_24, TweenInfo.new(0), {
            ["FieldOfView"] = 50
        }):Play()
        v_u_194[v_u_85].Humanoid.CameraOffset = v_u_194[v_u_85]:GetAttribute("CamOffset") or Vector3.new(0, 0, 0)
        v_u_24.CameraSubject = v_u_194[v_u_85]
        v_u_24.CFrame = v_u_194[v_u_85].PrimaryPart.CFrame
        v_u_24.CameraType = Enum.CameraType.Custom
        v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
        v_u_3:BindToRenderStep("CamConnection", Enum.RenderPriority.Last.Value, v_u_202)
    end
    v_u_120.CameraOverlay.Visible = true
    v_u_120.CameraOverlay.Noise:Play()
    game.Lighting.CameraCC.Enabled = true
    game.SoundService.GameSounds.Fx.CameraEffect.Enabled = true
    v_u_2:BindAction("PrevCam", v209, true, Enum.KeyCode.Q)
    v_u_2:BindAction("NextRight", v209, true, Enum.KeyCode.E)
end
function UnsetCamera()
    -- upvalues: (ref) v_u_84, (copy) v_u_3, (copy) v_u_2, (ref) v_u_120, (copy) v_u_24, (copy) v_u_22, (copy) v_u_60, (ref) v_u_97
    if v_u_84 then
        v_u_3:UnbindFromRenderStep("CamConnection")
        v_u_2:UnbindAction("PrevCam")
        v_u_2:UnbindAction("NextRight")
        v_u_120.CameraOverlay.Visible = false
        v_u_120.CameraOverlay.Noise:Stop()
        v_u_120.CameraOverlay.Haha.Playing = false
        game.Lighting.CameraCC.Enabled = false
        game.SoundService.GameSounds.Fx.CameraEffect.Enabled = false
        v_u_24.CameraSubject = v_u_22.Character
        v_u_24.FieldOfView = v_u_60
        v_u_24.CameraType = Enum.CameraType.Custom
        v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
        v_u_24.CFrame = v_u_97
        v_u_84 = false
    end
end
function InitializeDrone()
    -- upvalues: (ref) v_u_130, (ref) v_u_131, (ref) v_u_97, (copy) v_u_24, (copy) v_u_30, (ref) v_u_32, (ref) v_u_34
    v_u_130 = 0
    v_u_131 = 0
    Lean()
    v_u_97 = v_u_24.CFrame
    v_u_30:Enable()
    if not v_u_30.InDrone then
        unset()
        v_u_32 = 1
        setup(v_u_34)
    end
end
function UnsetDrone()
    -- upvalues: (copy) v_u_30, (copy) v_u_24, (copy) v_u_22, (copy) v_u_60, (ref) v_u_97
    if v_u_30.InDrone then
        v_u_30:Disable()
        v_u_24.CameraSubject = v_u_22.Character
        v_u_24.FieldOfView = v_u_60
        v_u_24.CameraType = Enum.CameraType.Custom
        v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
        v_u_24.CFrame = v_u_97
    end
end
function MoveSound()
    -- upvalues: (copy) v_u_142, (copy) v_u_18, (copy) v_u_23, (copy) v_u_5
    if v_u_142 then
        local v210 = v_u_18.Move:GetChildren()
        local v211 = v210[math.random(#v210)]:Clone()
        local v212 = v_u_23.ClientConfig:GetAttribute("Loudness")
        v211.Parent = v_u_142
        v211.PlaybackSpeed = math.random(30, 55) / 40
        v211.Volume = 0.5 * v212
        v211.RollOffMinDistance = 5 * v212
        v211.RollOffMaxDistance = 25 * v212
        v211:Play()
        v_u_5:AddItem(v211, v211.TimeLength)
    end
end
function SpeedCheck()
    -- upvalues: (copy) v_u_8, (copy) v_u_23, (copy) v_u_139, (copy) v_u_4, (ref) v_u_74, (ref) v_u_129, (ref) v_u_49, (ref) v_u_48, (ref) v_u_137, (ref) v_u_75
    if v_u_8:HasTag(v_u_23.Humanoid, "Interacting") then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)
        v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0), {
            ["WalkSpeed"] = 0
        }):Play()
        return
    elseif v_u_8:HasTag(v_u_23.Humanoid, "Slow") then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)
        v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0), {
            ["WalkSpeed"] = 2 * v_u_23.ClientConfig:GetAttribute("Mobility")
        }):Play()
        return
    elseif v_u_74 and (v_u_129 == 0 and not v_u_49) then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
        if v_u_48 and not v_u_48.CanRun then
            v_u_74 = false
            if v_u_137 then
                v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                    ["WalkSpeed"] = 5 * v_u_23.ClientConfig:GetAttribute("Mobility")
                }):Play()
            else
                v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                    ["WalkSpeed"] = 10 * v_u_23.ClientConfig:GetAttribute("Mobility")
                }):Play()
            end
        else
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(1), {
                ["WalkSpeed"] = 14 * v_u_23.ClientConfig:GetAttribute("Mobility")
            }):Play()
            return
        end
    elseif v_u_129 == 0 then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
        if v_u_137 then
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 5 * v_u_23.ClientConfig:GetAttribute("Mobility")
            }):Play()
            return
        elseif v_u_75 then
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 10 * v_u_23.ClientConfig:GetAttribute("Mobility") / 1.35
            }):Play()
        else
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 10 * v_u_23.ClientConfig:GetAttribute("Mobility")
            }):Play()
        end
    elseif v_u_129 == 1 then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)
        if v_u_137 then
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 3 * v_u_23.ClientConfig:GetAttribute("Mobility")
            }):Play()
            return
        elseif v_u_75 then
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 6 * v_u_23.ClientConfig:GetAttribute("Mobility") / 1.35
            }):Play()
        else
            v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0.25), {
                ["WalkSpeed"] = 6 * v_u_23.ClientConfig:GetAttribute("Mobility")
            }):Play()
        end
    elseif v_u_129 == 2 then
        v_u_139:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)
        v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(0), {
            ["WalkSpeed"] = 2 * v_u_23.ClientConfig:GetAttribute("Mobility")
        }):Play()
    end
end
local function v_u_215()
    -- upvalues: (ref) v_u_40, (copy) v_u_24
    if v_u_40 then
        for _, v213 in ipairs(v_u_40:GetDescendants()) do
            if v213:IsA("BasePart") and v213.Name == "SightMark" then
                local v214 = v213.CFrame:pointToObjectSpace(v_u_24.CFrame.Position) / v213.Size
                v213.SurfaceGui.Border.Scope.Position = UDim2.new(0.5 + v214.x, 0, 0.5 - v214.y, 0)
            end
        end
    end
end
local function v_u_219(p216, p217)
    if p216 then
        for _, v218 in ipairs(p216:GetDescendants()) do
            if v218:IsA("BasePart") and v218.Name == "ADSmesh" then
                v218.Transparency = p217
            end
            if v218:IsA("Texture") and v218.Parent.Name == "ADSmesh" then
                v218.Transparency = p217
            end
        end
    end
end
local function v_u_223(p220)
    -- upvalues: (ref) v_u_48, (ref) v_u_40, (copy) v_u_8, (copy) v_u_22, (ref) v_u_101, (copy) v_u_1, (copy) v_u_64, (copy) v_u_4, (copy) v_u_24, (copy) v_u_113, (copy) v_u_104, (ref) v_u_120, (copy) v_u_123, (copy) v_u_62, (copy) v_u_60
    SpeedCheck()
    if v_u_48 and v_u_40 then
        if p220 then
            v_u_8:AddTag(v_u_22, "ADS")
            if v_u_101.Aim then
                v_u_101.Aim:Play(0.15)
            end
            for _, v221 in pairs(v_u_101) do
                if v221 ~= v_u_101.Aim and v221 ~= v_u_101.Reload then
                    v221:Stop(0.15)
                end
            end
            v_u_1.MouseDeltaSensitivity = v_u_64
            if v_u_40:FindFirstChild("Handle") and v_u_40.Handle:FindFirstChild("AimDown") then
                v_u_40.Handle.AimDown:Play()
            end
            v_u_4:Create(v_u_24, v_u_113, {
                ["FieldOfView"] = v_u_104.ZoomValue
            }):Play()
            v_u_4:Create(v_u_120.Efeitos.Aim, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["ImageTransparency"] = 0
            }):Play()
            v_u_4:Create(v_u_123.Up, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["BackgroundTransparency"] = 1
            }):Play()
            v_u_4:Create(v_u_123.Down, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["BackgroundTransparency"] = 1
            }):Play()
            v_u_4:Create(v_u_123.Left, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["BackgroundTransparency"] = 1
            }):Play()
            v_u_4:Create(v_u_123.Right, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["BackgroundTransparency"] = 1
            }):Play()
            v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["ImageTransparency"] = 1
            }):Play()
            return
        else
            v_u_8:RemoveTag(v_u_22, "ADS")
            if v_u_101.Idle then
                v_u_101.Idle:Play(0.15)
            end
            for _, v222 in pairs(v_u_101) do
                if v222 ~= v_u_101.Idle and v222 ~= v_u_101.Reload then
                    v222:Stop(0.15)
                end
            end
            v_u_1.MouseDeltaSensitivity = v_u_62
            if v_u_40:FindFirstChild("Handle") and v_u_40.Handle:FindFirstChild("AimUp") then
                v_u_40.Handle.AimUp:Play()
            end
            v_u_4:Create(v_u_24, v_u_113, {
                ["FieldOfView"] = v_u_60
            }):Play()
            v_u_4:Create(v_u_120.Efeitos.Aim, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                ["ImageTransparency"] = 1
            }):Play()
            if v_u_48.CrossHair then
                v_u_4:Create(v_u_123.Up, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["BackgroundTransparency"] = 0
                }):Play()
                v_u_4:Create(v_u_123.Down, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["BackgroundTransparency"] = 0
                }):Play()
                v_u_4:Create(v_u_123.Left, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["BackgroundTransparency"] = 0
                }):Play()
                v_u_4:Create(v_u_123.Right, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["BackgroundTransparency"] = 0
                }):Play()
            end
            if v_u_48.CenterDot then
                v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["ImageTransparency"] = 0
                }):Play()
            else
                v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                    ["ImageTransparency"] = 1
                }):Play()
            end
        end
    else
        return
    end
end
local function v315(p224)
    -- upvalues: (ref) v_u_102, (copy) v_u_188, (copy) v_u_124, (ref) v_u_111, (copy) v_u_193, (ref) v_u_75, (copy) v_u_1, (copy) v_u_126, (ref) v_u_41, (ref) v_u_40, (ref) v_u_48, (copy) v_u_22, (ref) v_u_42, (copy) v_u_24, (copy) v_u_127, (copy) v_u_66, (ref) v_u_105, (ref) v_u_110, (ref) v_u_112, (ref) v_u_106, (ref) v_u_73, (ref) v_u_72, (ref) v_u_74, (ref) v_u_49, (ref) v_u_98, (ref) v_u_81, (copy) v_u_109, (ref) v_u_99, (copy) v_u_219, (ref) v_u_84, (copy) v_u_30, (ref) v_u_68, (ref) v_u_69, (ref) v_u_70, (ref) v_u_71, (ref) v_u_55, (copy) v_u_104, (copy) v_u_123, (ref) v_u_57, (ref) v_u_76, (ref) v_u_56, (ref) v_u_92, (ref) v_u_91, (copy) v_u_114, (ref) v_u_94, (ref) v_u_144, (copy) v_u_11, (copy) v_u_215
    v_u_102 = 1 - 5e-7 ^ p224
    v_u_188(v_u_102)
    HeadMovement()
    local v225 = v_u_124:update(p224)
    local v226 = p224 * 20
    v_u_111 = v_u_111 * CFrame.Angles(v225.X * v226, v225.Y * v226, v225.Z * v226)
    v_u_193(p224)
    local v227 = v_u_75 and 2 or 1
    local v228 = v_u_1:GetMouseDelta()
    local v229 = v_u_126
    local v230 = v228.x / (400 * v227)
    local v231 = v228.y / (400 * v227)
    v229:shove((Vector3.new(v230, v231)))
    if v_u_41 and v_u_40 then
        if v_u_48 then
            if v_u_48.OnUpdate then
                v_u_48.OnUpdate(v_u_22, v_u_41)
            end
            local v232 = v_u_126:update(p224)
            local v233 = v232.X
            local v234 = math.clamp(v233, -0.35, 0.35)
            local v235 = v232.Y
            local v236 = math.clamp(v235, -0.35, 0.35)
            local v237 = CFrame.Angles(v236, v234, v234)
            v_u_42.CFrame = v_u_24.CFrame * CFrame.fromAxisAngle(Vector3.new(0, 0, 1), v_u_127.cornerPeek.p) * CFrame.new(0, 0, -0.5 * v_u_66) * v_u_105 * v_u_110 * v_u_112 * v237:inverse()
            if not v_u_48.GunModelFixed then
                v_u_40:PivotTo(v_u_41.PrimaryPart.CFrame * v_u_106)
            end
            if v_u_73 then
                if v_u_75 then
                    local v238 = v_u_110
                    local v239 = CFrame.new
                    local v240 = 0.005 * (v_u_72 / 10)
                    local v241 = os.clock() * 8
                    local v242 = v240 * math.sin(v241)
                    local v243 = 0.005 * (v_u_72 / 10)
                    local v244 = os.clock() * 16
                    local v245 = v239(v242, v243 * math.cos(v244), 0)
                    local v246 = CFrame.Angles
                    local v247 = 0.25 * (v_u_72 / 10)
                    local v248 = os.clock() * 16
                    local v249 = v247 * math.sin(v248)
                    local v250 = math.rad(v249)
                    local v251 = 0.25 * (v_u_72 / 10)
                    local v252 = os.clock() * 8
                    local v253 = v251 * math.cos(v252)
                    v_u_110 = v238:Lerp(v245 * v246(v250, math.rad(v253), 0), v_u_102)
                elseif v_u_74 and (v_u_48 and (v_u_48.CanRun and not v_u_49)) then
                    local v254 = v_u_110
                    local v255 = CFrame.new
                    local v256 = 0.075 * (v_u_72 / 10)
                    local v257 = os.clock() * 8
                    local v258 = v256 * math.sin(v257)
                    local v259 = 0.075 * (v_u_72 / 10)
                    local v260 = os.clock() * 16
                    local v261 = v255(v258, v259 * math.cos(v260), 0)
                    local v262 = CFrame.Angles
                    local v263 = 1 * (v_u_72 / 10)
                    local v264 = os.clock() * 16
                    local v265 = v263 * math.sin(v264)
                    local v266 = math.rad(v265)
                    local v267 = 1 * (v_u_72 / 10)
                    local v268 = os.clock() * 8
                    local v269 = v267 * math.cos(v268)
                    local v270 = math.rad(v269)
                    local v271 = (v_u_98.X + v_u_98.Y) * v_u_72
                    local v272 = math.clamp(v271, -5, 5)
                    v_u_110 = v254:Lerp(v261 * v262(v266, v270, -math.rad(v272)), v_u_102)
                else
                    local v273 = v_u_110
                    local v274 = CFrame.new
                    local v275 = 0.025 * (v_u_72 / 10)
                    local v276 = os.clock() * 8
                    local v277 = v275 * math.sin(v276)
                    local v278 = 0.025 * (v_u_72 / 10)
                    local v279 = os.clock() * 16
                    local v280 = v274(v277, v278 * math.cos(v279), 0)
                    local v281 = CFrame.Angles
                    local v282 = 1 * (v_u_72 / 10)
                    local v283 = os.clock() * 16
                    local v284 = v282 * math.sin(v283)
                    local v285 = math.rad(v284)
                    local v286 = 1 * (v_u_72 / 10)
                    local v287 = os.clock() * 8
                    local v288 = v286 * math.cos(v287)
                    local v289 = math.rad(v288)
                    local v290 = (v_u_98.X + v_u_98.Y) * v_u_72
                    local v291 = math.clamp(v290, -5, 5)
                    v_u_110 = v273:Lerp(v280 * v281(v285, v289, -math.rad(v291)), v_u_102)
                end
            else
                local v292 = v_u_110
                local v293 = CFrame.new
                local v294 = os.clock() * 1.5
                local v295 = 0.005 * math.sin(v294)
                local v296 = os.clock() * 2.5
                v_u_110 = v292:Lerp(v293(v295, 0.005 * math.cos(v296), 0), v_u_102)
            end
            if v_u_75 and v_u_81 then
                if v_u_40:FindFirstChild("AimPart") then
                    v_u_112 = v_u_112:Lerp(v_u_112 * v_u_109 * CFrame.new(v_u_40.AimPart.CFrame:toObjectSpace(v_u_24.CFrame).Position), v_u_102)
                    v_u_99 = v_u_99:Lerp(Vector2.new(1, 0), v_u_102)
                    if v_u_99.X > 0.9 then
                        v_u_219(v_u_40, 1)
                    end
                end
            elseif not (v_u_84 or v_u_30.InDrone) then
                v_u_112 = v_u_112:Lerp(CFrame.new(), v_u_102)
                v_u_99 = v_u_99:Lerp(Vector2.new(0, 0), v_u_102)
                v_u_219(v_u_40, 0)
            end
            v_u_105 = v_u_105:Lerp(v_u_48.MainCFrame * v_u_111, v_u_102)
            local v297 = v_u_111
            local v298 = CFrame.new()
            local v299 = CFrame.Angles
            local v300 = v_u_124.Position.X
            local v301 = math.rad(v300)
            local v302 = v_u_124.Position.Y
            local v303 = math.rad(v302)
            local v304 = v_u_124.Position.Z
            v_u_111 = v297:Lerp(v298 * v299(v301, v303, (math.rad(v304))), v_u_102)
            if v_u_48.CrossHair then
                if v_u_75 then
                    v_u_68 = v_u_68:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                    v_u_69 = v_u_69:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                    v_u_70 = v_u_70:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                    v_u_71 = v_u_71:Lerp(UDim2.new(0.5, 0, 0.5, 0), v_u_102)
                else
                    local v305 = (v_u_48.CrosshairOffset + v_u_55 + v_u_72 * v_u_48.WalkMult * v_u_104.WalkMult) / 50 / 10
                    v_u_68 = v_u_68:Lerp(UDim2.new(0.5, 0, 0.5 - v305, 0), 0.5)
                    v_u_69 = v_u_69:Lerp(UDim2.new(0.5, 0, 0.5 + v305, 0), 0.5)
                    v_u_70 = v_u_70:Lerp(UDim2.new(0.5 - v305, 0, 0.5, 0), 0.5)
                    v_u_71 = v_u_71:Lerp(UDim2.new(0.5 + v305, 0, 0.5, 0), 0.5)
                end
                v_u_123.Up.Position = v_u_68
                v_u_123.Down.Position = v_u_69
                v_u_123.Left.Position = v_u_70
                v_u_123.Right.Position = v_u_71
            else
                v_u_68 = v_u_68:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                v_u_69 = v_u_69:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                v_u_70 = v_u_70:Lerp(UDim2.new(0.5, 0, 0.5, 0), 0.2)
                v_u_71 = v_u_71:Lerp(UDim2.new(0.5, 0, 0.5, 0), v_u_102)
                v_u_123.Up.Position = v_u_68
                v_u_123.Down.Position = v_u_69
                v_u_123.Left.Position = v_u_70
                v_u_123.Right.Position = v_u_71
            end
            if v_u_55 then
                local v306 = os.clock()
                if v306 - v_u_57 > 60 / v_u_48.ShootRate * 2 and (not v_u_76 and v_u_55 > v_u_48.MinSpread * v_u_104.MinSpread) then
                    local v307 = v_u_48.MinSpread * v_u_104.MinSpread
                    local v308 = v_u_55 - v_u_48.AimInaccuracyDecrease * v_u_104.AimInaccuracyDecrease
                    v_u_55 = math.max(v307, v308)
                end
                if v306 - v_u_57 > 60 / v_u_48.ShootRate * 1.5 and (not v_u_76 and v_u_56 > v_u_48.MinRecoilPower * v_u_104.MinRecoilPower) then
                    local v309 = v_u_48.MinRecoilPower * v_u_104.MinRecoilPower
                    local v310 = v_u_56 - v_u_48.RecoilPowerStepAmount * v_u_104.RecoilPowerStepAmount
                    v_u_56 = math.max(v309, v310)
                end
            end
            if v_u_92 and v_u_91:FindFirstChild("LaserPoint") then
                local v311 = Ray.new(v_u_24.CFrame.Position, v_u_91.LaserPoint.CFrame.LookVector * 1000)
                local v312, v313, v314 = workspace:FindPartOnRayWithIgnoreList(v311, v_u_114, false, true)
                if v312 then
                    v_u_94.CFrame = CFrame.new(v313, v313 + v314)
                else
                    v_u_94.CFrame = CFrame.new(v_u_24.CFrame.Position + v_u_91.LaserPoint.CFrame.LookVector * 2000, v_u_91.LaserPoint.CFrame.LookVector)
                end
                if v_u_144 then
                    v_u_11.SVLaser:FireServer(v313, v314, 1, v_u_94.Color, false)
                end
            end
            v_u_215()
        end
    else
        return
    end
end
if v_u_8:HasTag(v_u_22, "Alive") then
    v_u_120.Enabled = true
    v_u_3:BindToRenderStep("Render_Viewmodel", Enum.RenderPriority.Last.Value + 1, v315)
    local function v_u_318(p316, p317, _)
        -- upvalues: (ref) v_u_48, (ref) v_u_81, (ref) v_u_32, (ref) v_u_95, (ref) v_u_96, (ref) v_u_78
        if p316 == "Fire" and p317 == Enum.UserInputState.Begin then
            if not v_u_48 then
                return
            end
            if v_u_48.Type == "Gun" and v_u_81 then
                Shoot()
                return
            end
            if v_u_48.Type == "Melee" then
                if v_u_32 ~= 5 then
                    Melee()
                end
            end
            if v_u_48.Type == "Grenade" then
                if not v_u_95 then
                    v_u_96 = true
                    Grenade()
                end
            end
            if v_u_48.Type == "Placeable" then
                if not v_u_95 then
                    Placeable()
                end
            end
            if v_u_48.Type == "Gadget" then
                Gadget()
                return
            end
        elseif p316 == "Fire" and p317 == Enum.UserInputState.End then
            v_u_78 = false
            v_u_96 = false
        end
    end
    local function v_u_321(p319, p320, _)
        -- upvalues: (ref) v_u_81, (ref) v_u_103, (ref) v_u_48, (ref) v_u_74, (copy) v_u_59, (ref) v_u_75, (copy) v_u_223
        if p319 == "ADS" and (p320 == Enum.UserInputState.Begin and v_u_81) then
            if os.clock() - v_u_103 <= 0.25 then
                return
            end
            if v_u_48 and (v_u_48.canAim and not v_u_74) then
                if v_u_59 then
                    if v_u_59.toggleADS == false then
                        v_u_75 = true
                        v_u_223(v_u_75)
                    else
                        v_u_75 = not v_u_75
                        v_u_223(v_u_75)
                    end
                else
                    v_u_75 = not v_u_75
                    v_u_223(v_u_75)
                end
            end
        end
        if p319 == "ADS" and (p320 == Enum.UserInputState.End and (v_u_81 and (v_u_48 and (v_u_48.canAim and (not v_u_74 and (v_u_59 and v_u_59.toggleADS == false)))))) then
            v_u_75 = false
            v_u_223(v_u_75)
        end
    end
    local function v_u_324(p322, p323, _)
        -- upvalues: (ref) v_u_77, (ref) v_u_48, (ref) v_u_82
        if p322 == "Reload" and p323 == Enum.UserInputState.Begin then
            if not v_u_77 then
                Reload()
                return
            end
            if v_u_77 and v_u_48.ShellInsert then
                v_u_82 = true
            end
        end
    end
    local function v_u_327(p325, p326, _)
        -- upvalues: (ref) v_u_95, (ref) v_u_96, (ref) v_u_77, (ref) v_u_79
        if p325 == "Melee" and (p326 == Enum.UserInputState.Begin and (not v_u_95 and (not v_u_96 and (not v_u_77 and v_u_79)))) then
            Melee()
        end
    end
    local function v330(p328, p329, _)
        -- upvalues: (copy) v_u_22, (copy) v_u_8, (copy) v_u_23, (ref) v_u_79, (ref) v_u_80, (ref) v_u_95, (ref) v_u_32, (ref) v_u_41, (ref) v_u_33, (ref) v_u_34, (ref) v_u_35, (ref) v_u_38, (ref) v_u_36, (ref) v_u_39, (ref) v_u_37, (ref) v_u_84
        if v_u_22.Character and (v_u_22.Character:FindFirstChild("Humanoid") and v_u_22.Character.Humanoid.Health > 0) then
            if v_u_8:HasTag(v_u_23.Humanoid, "Interacting") then
                return
            elseif v_u_79 and v_u_80 then
                if not v_u_95 then
                    if p328 == "EquipPrimary" and (p329 == Enum.UserInputState.Begin and v_u_32 ~= 1) then
                        if v_u_41 then
                            unset()
                        end
                        v_u_32 = 1
                        v_u_33 = 1
                        setup(v_u_34)
                    end
                    if p328 == "EquipSecondary" and (p329 == Enum.UserInputState.Begin and v_u_32 ~= 2) then
                        if v_u_41 then
                            unset()
                        end
                        v_u_32 = 2
                        v_u_33 = 2
                        setup(v_u_35)
                    end
                    if p328 == "EquipUtility" and (p329 == Enum.UserInputState.Begin and v_u_32 ~= 3) then
                        if v_u_38 <= 0 then
                            return
                        end
                        if v_u_41 then
                            unset()
                        end
                        v_u_32 = 3
                        setup(v_u_36)
                    end
                    if p328 == "EquipGadget" and (p329 == Enum.UserInputState.Begin and v_u_32 ~= 4) then
                        if v_u_39 <= 0 then
                            return
                        end
                        if v_u_41 then
                            unset()
                        end
                        v_u_32 = 4
                        setup(v_u_37)
                    end
                    if p328 == "EquipCamera" and (p329 == Enum.UserInputState.Begin and v_u_32 ~= 5) then
                        if v_u_41 then
                            unset()
                        end
                        v_u_32 = 5
                        setup("Camera")
                        if v_u_22.TeamColor == game.Teams.Defenders.TeamColor then
                            v_u_84 = true
                            InitializeCamera()
                            return
                        end
                        if v_u_22.TeamColor == game.Teams.Attackers.TeamColor then
                            InitializeDrone()
                        end
                    end
                end
            else
                return
            end
        else
            return
        end
    end
    local function v333(p331, p332, _)
        -- upvalues: (ref) v_u_129, (ref) v_u_138, (ref) v_u_74, (copy) v_u_59, (ref) v_u_130, (ref) v_u_131
        if p331 == "LeanLeft" and (p332 == Enum.UserInputState.Begin and (v_u_129 ~= 2 and (v_u_138 and not v_u_74))) then
            if v_u_59 and v_u_59.toggleLean == false then
                v_u_130 = -1
                v_u_131 = -1
                Lean()
            else
                if v_u_130 == 0 or v_u_130 == 1 then
                    v_u_130 = -1
                    v_u_131 = -1
                else
                    v_u_130 = 0
                    v_u_131 = 0
                end
                Lean()
            end
        end
        if p331 == "LeanLeft" and (p332 == Enum.UserInputState.End and (v_u_129 ~= 2 and (v_u_138 and (not v_u_74 and (v_u_59 and (v_u_59.toggleLean == false and v_u_130 == -1)))))) then
            v_u_130 = 0
            v_u_131 = 0
            Lean()
        end
        if p331 == "LeanRight" and (p332 == Enum.UserInputState.Begin and (v_u_129 ~= 2 and (v_u_138 and not v_u_74))) then
            if v_u_59 and v_u_59.toggleLean == false then
                v_u_130 = 1
                v_u_131 = 1
                Lean()
            else
                if v_u_130 == 0 or v_u_130 == -1 then
                    v_u_130 = 1
                    v_u_131 = 1
                else
                    v_u_130 = 0
                    v_u_131 = 0
                end
                Lean()
            end
        end
        if p331 == "LeanRight" and (p332 == Enum.UserInputState.End and (v_u_129 ~= 2 and (v_u_138 and (not v_u_74 and (v_u_59 and (v_u_59.toggleLean == false and v_u_130 == 1)))))) then
            v_u_130 = 0
            v_u_131 = 0
            Lean()
        end
    end
    local function v339(p334, p335, _)
        -- upvalues: (ref) v_u_138, (ref) v_u_103, (ref) v_u_74, (ref) v_u_49, (ref) v_u_84, (copy) v_u_30, (ref) v_u_129, (ref) v_u_135, (ref) v_u_136, (ref) v_u_132, (ref) v_u_75, (copy) v_u_223, (ref) v_u_131, (ref) v_u_130, (ref) v_u_137, (ref) v_u_73, (ref) v_u_48, (ref) v_u_77, (ref) v_u_101
        if p334 == "Prone" and (p335 == Enum.UserInputState.Begin and v_u_138) then
            if os.clock() - v_u_103 < 0.2 then
                return
            end
            if v_u_74 and not v_u_49 then
                return
            end
            if v_u_84 or v_u_30.InDrone then
                return
            end
            if v_u_129 == 2 then
                v_u_103 = os.clock()
                v_u_135 = false
                v_u_136 = false
                v_u_129 = 0
                v_u_132 = 0
                Stand()
                MoveSound()
                v_u_75 = false
                v_u_223(v_u_75)
            else
                v_u_103 = os.clock()
                v_u_135 = false
                v_u_136 = true
                v_u_129 = 2
                v_u_131 = 0
                v_u_132 = -3.25
                v_u_130 = 0
                Lean()
                Prone()
                MoveSound()
                v_u_75 = false
                v_u_223(v_u_75)
            end
            SpeedCheck()
        end
        if p334 == "Crouch" and (p335 == Enum.UserInputState.Begin and v_u_138) then
            if v_u_74 and not v_u_49 then
                return
            end
            if v_u_84 or v_u_30.InDrone then
                return
            end
            if v_u_129 == 1 then
                v_u_135 = false
                v_u_136 = false
                v_u_129 = 0
                v_u_132 = 0
                Stand()
                MoveSound()
            elseif v_u_129 == 2 then
                v_u_103 = os.clock()
                v_u_135 = true
                v_u_136 = false
                v_u_129 = 1
                v_u_132 = -1
                Crouch()
                MoveSound()
                v_u_75 = false
                v_u_223(v_u_75)
            else
                v_u_135 = true
                v_u_136 = false
                v_u_129 = 1
                v_u_132 = -1
                Crouch()
                MoveSound()
            end
            SpeedCheck()
        end
        if p334 == "ToggleWalk" and (p335 == Enum.UserInputState.Begin and v_u_138) then
            if v_u_84 or v_u_30.InDrone then
                return
            end
            v_u_137 = not v_u_137
            SpeedCheck()
        end
        if p334 == "Run" and p335 == Enum.UserInputState.Begin then
            if v_u_49 then
                v_u_74 = true
                v_u_130 = 0
                v_u_131 = 0
                Lean()
                SpeedCheck()
                if v_u_75 then
                    v_u_75 = false
                    v_u_223(v_u_75)
                end
                if not v_u_77 and (v_u_48 and (v_u_48.Type ~= "melee" and v_u_48.Type ~= "Grenade")) then
                    if v_u_101.Sprint then
                        v_u_101.Sprint:Play(0.15)
                    end
                    for _, v336 in pairs(v_u_101) do
                        if v336 ~= v_u_101.Sprint and v336 ~= v_u_101.Reload then
                            v336:Stop(0.15)
                        end
                    end
                    SprintAnim()
                    return
                end
            else
                if not v_u_73 then
                    return
                end
                if v_u_48 and not v_u_48.CanRun then
                    return
                end
                if v_u_84 or v_u_30.InDrone then
                    return
                end
                v_u_74 = true
                if v_u_129 ~= 0 then
                    MoveSound()
                end
                Stand()
                v_u_129 = 0
                v_u_130 = 0
                v_u_131 = 0
                v_u_132 = 0
                v_u_137 = false
                Lean()
                SpeedCheck()
                if v_u_75 then
                    v_u_75 = false
                    v_u_223(v_u_75)
                end
                if not v_u_77 and (v_u_48 and (v_u_48.Type ~= "melee" and v_u_48.Type ~= "Grenade")) then
                    if v_u_101.Sprint then
                        v_u_101.Sprint:Play(0.15)
                    end
                    for _, v337 in pairs(v_u_101) do
                        if v337 ~= v_u_101.Sprint and v337 ~= v_u_101.Reload then
                            v337:Stop(0.15)
                        end
                    end
                    SprintAnim()
                    return
                end
            end
        elseif p334 == "Run" and (p335 == Enum.UserInputState.End and v_u_74) then
            v_u_74 = false
            Stand()
            SpeedCheck()
            if not v_u_77 and (v_u_48 and (v_u_48.Type ~= "melee" and v_u_48.Type ~= "Grenade")) then
                if v_u_101.Idle then
                    v_u_101.Idle:Play(0.15)
                end
                for _, v338 in pairs(v_u_101) do
                    if v338 ~= v_u_101.Idle and v338 ~= v_u_101.Reload then
                        v338:Stop(0.15)
                    end
                end
                IdleAnim()
            end
        end
    end
    function resetMods()
        -- upvalues: (copy) v_u_104
        v_u_104.camRecoilMod.RecoilUp = 1
        v_u_104.camRecoilMod.RecoilLeft = 1
        v_u_104.camRecoilMod.RecoilRight = 1
        v_u_104.camRecoilMod.RecoilTilt = 1
        v_u_104.gunRecoilMod.RecoilUp = 1
        v_u_104.gunRecoilMod.RecoilTilt = 1
        v_u_104.gunRecoilMod.RecoilLeft = 1
        v_u_104.gunRecoilMod.RecoilRight = 1
        v_u_104.AimRM = 1
        v_u_104.SpreadRM = 1
        v_u_104.DamageMod = 1
        v_u_104.minDamageMod = 1
        v_u_104.MinRecoilPower = 1
        v_u_104.MaxRecoilPower = 1
        v_u_104.RecoilPowerStepAmount = 1
        v_u_104.MinSpread = 1
        v_u_104.MaxSpread = 1
        v_u_104.AimInaccuracyStepAmount = 1
        v_u_104.AimInaccuracyDecrease = 1
        v_u_104.WalkMult = 1
        v_u_104.MuzzleVelocity = 1
    end
    function setMods(p340)
        -- upvalues: (copy) v_u_104
        v_u_104.camRecoilMod.RecoilUp = v_u_104.camRecoilMod.RecoilUp * p340.camRecoil.RecoilUp
        v_u_104.camRecoilMod.RecoilLeft = v_u_104.camRecoilMod.RecoilLeft * p340.camRecoil.RecoilLeft
        v_u_104.camRecoilMod.RecoilRight = v_u_104.camRecoilMod.RecoilRight * p340.camRecoil.RecoilRight
        v_u_104.camRecoilMod.RecoilTilt = v_u_104.camRecoilMod.RecoilTilt * p340.camRecoil.RecoilTilt
        v_u_104.gunRecoilMod.RecoilUp = v_u_104.gunRecoilMod.RecoilUp * p340.gunRecoil.RecoilUp
        v_u_104.gunRecoilMod.RecoilTilt = v_u_104.gunRecoilMod.RecoilTilt * p340.gunRecoil.RecoilTilt
        v_u_104.gunRecoilMod.RecoilLeft = v_u_104.gunRecoilMod.RecoilLeft * p340.gunRecoil.RecoilLeft
        v_u_104.gunRecoilMod.RecoilRight = v_u_104.gunRecoilMod.RecoilRight * p340.gunRecoil.RecoilRight
        local v341 = v_u_104
        local v342 = v_u_104.AimRM + p340.AimRecoilReduction
        v341.AimRM = math.max(v342, 0.01)
        v_u_104.SpreadRM = v_u_104.SpreadRM * p340.AimSpreadReduction
        v_u_104.DamageMod = v_u_104.DamageMod * p340.DamageMod
        v_u_104.minDamageMod = v_u_104.minDamageMod * p340.minDamageMod
        v_u_104.MinRecoilPower = v_u_104.MinRecoilPower * p340.MinRecoilPower
        v_u_104.MaxRecoilPower = v_u_104.MaxRecoilPower * p340.MaxRecoilPower
        v_u_104.RecoilPowerStepAmount = v_u_104.RecoilPowerStepAmount * p340.RecoilPowerStepAmount
        v_u_104.MinSpread = v_u_104.MinSpread * p340.MinSpread
        v_u_104.MaxSpread = v_u_104.MaxSpread * p340.MaxSpread
        v_u_104.AimInaccuracyStepAmount = v_u_104.AimInaccuracyStepAmount * p340.AimInaccuracyStepAmount
        v_u_104.AimInaccuracyDecrease = v_u_104.AimInaccuracyDecrease * p340.AimInaccuracyDecrease
        v_u_104.WalkMult = v_u_104.WalkMult * p340.WalkMult
        v_u_104.MuzzleVelocity = v_u_104.MuzzleVelocity * p340.MuzzleVelocityMod
    end
    function loadAttachment(p343)
        -- upvalues: (ref) v_u_48, (ref) v_u_50, (copy) v_u_16, (ref) v_u_86, (copy) v_u_15, (copy) v_u_104, (ref) v_u_51, (ref) v_u_87, (ref) v_u_88, (ref) v_u_89, (ref) v_u_52, (ref) v_u_90, (ref) v_u_53, (ref) v_u_91, (ref) v_u_92, (ref) v_u_94, (copy) v_u_18
        if p343 and p343:FindFirstChild("Nodes") ~= nil then
            if p343.Nodes:FindFirstChild("Sight") ~= nil and v_u_48.SightAtt ~= "" then
                v_u_50 = require(v_u_16[v_u_48.SightAtt])
                v_u_86 = v_u_15[v_u_48.SightAtt]:Clone()
                v_u_86.Parent = p343
                v_u_86:SetPrimaryPartCFrame(p343.Nodes.Sight.CFrame)
                if v_u_50.SightZoom > 0 then
                    v_u_104.ZoomValue = v_u_50.SightZoom
                    p343.AimPart.CFrame = v_u_86.AimPos.CFrame
                else
                    local v344 = p343.AimPart.CFrame:ToObjectSpace(v_u_86.AimPos.CFrame).Position.Z
                    local v345 = math.max(v344, 0)
                    v_u_86:SetPrimaryPartCFrame(p343.Nodes.Sight.CFrame * CFrame.new(0, 0, -v345))
                    p343.AimPart.CFrame = CFrame.new(v_u_86.AimPos.Position.X, v_u_86.AimPos.Position.Y, p343.AimPart.Position.Z) * v_u_86.AimPos.CFrame.Rotation
                end
                setMods(v_u_50)
                for _, v346 in pairs(p343:GetChildren()) do
                    if v346.Name == "IS" then
                        v346:Destroy()
                    end
                end
            end
            if p343.Nodes:FindFirstChild("Barrel") ~= nil and v_u_48.BarrelAtt ~= "" then
                v_u_51 = require(v_u_16[v_u_48.BarrelAtt])
                v_u_87 = v_u_15[v_u_48.BarrelAtt]:Clone()
                v_u_87.Parent = p343
                v_u_87:SetPrimaryPartCFrame(p343.Nodes.Barrel.CFrame)
                if v_u_87:FindFirstChild("BarrelPos") ~= nil then
                    p343.Handle.Muzzle.WorldCFrame = v_u_87.BarrelPos.CFrame
                end
                v_u_88 = v_u_51.IsSuppressor
                v_u_89 = v_u_51.IsFlashHider
                setMods(v_u_51)
            end
            if p343.Nodes:FindFirstChild("UnderBarrel") ~= nil and v_u_48.UnderBarrelAtt ~= "" then
                v_u_52 = require(v_u_16[v_u_48.UnderBarrelAtt])
                v_u_90 = v_u_15[v_u_48.UnderBarrelAtt]:Clone()
                v_u_90.Parent = p343
                v_u_90:SetPrimaryPartCFrame(p343.Nodes.UnderBarrel.CFrame)
                setMods(v_u_52)
            end
            if p343.Nodes:FindFirstChild("Other") ~= nil and v_u_48.OtherAtt ~= "" then
                v_u_53 = require(v_u_16[v_u_48.OtherAtt])
                v_u_91 = v_u_15[v_u_48.OtherAtt]:Clone()
                v_u_91.Parent = p343
                v_u_91:SetPrimaryPartCFrame(p343.Nodes.Other.CFrame)
                setMods(v_u_53)
                v_u_92 = v_u_53.EnableLaser
                if v_u_92 then
                    v_u_94 = Instance.new("Part", v_u_91.LaserPoint)
                    v_u_94.Size = Vector3.new(0.2, 0.2, 0.05)
                    v_u_94.CanCollide = false
                    v_u_94.Color = v_u_91.LaserPoint.Color
                    v_u_94.Material = Enum.Material.Neon
                    v_u_94.Transparency = 1
                    local v347 = Instance.new("Attachment", v_u_94)
                    v347.CFrame = CFrame.new(0, 0.2, -0.05)
                    local v348 = Instance.new("Attachment", v_u_94)
                    v348.CFrame = CFrame.new(0, -0.2, -0.05)
                    local v349 = Instance.new("Trail", v_u_94)
                    v349.Color = ColorSequence.new(v_u_94.Color)
                    v349.LightEmission = 1
                    v349.LightInfluence = 0
                    v349.Lifetime = 0.05
                    v349.MaxLength = 0
                    v349.MinLength = 0
                    v349.Transparency = NumberSequence.new(0, 1)
                    v349.WidthScale = NumberSequence.new(0.25, 0)
                    v349.Attachment0 = v347
                    v349.Attachment1 = v348
                    local v350 = v_u_18.LaserDot:Clone()
                    v350.Parent = v_u_94
                    v350.ImageLabel.ImageColor3 = v_u_94.Color
                    v350.Adornee = v_u_94
                    v350.Enabled = true
                end
            end
        end
    end
    function setup(p351)
        -- upvalues: (copy) v_u_22, (copy) v_u_139, (ref) v_u_101, (ref) v_u_49, (ref) v_u_35, (copy) v_u_14, (ref) v_u_48, (ref) v_u_40, (copy) v_u_11, (copy) v_u_140, (ref) v_u_41, (copy) v_u_13, (ref) v_u_42, (ref) v_u_45, (ref) v_u_46, (ref) v_u_47, (copy) v_u_24, (ref) v_u_105, (ref) v_u_106, (ref) v_u_107, (ref) v_u_108, (copy) v_u_4, (copy) v_u_123, (ref) v_u_43, (ref) v_u_44, (copy) v_u_104, (ref) v_u_55, (ref) v_u_56, (copy) v_u_31, (ref) v_u_34, (copy) v_u_29, (copy) v_u_2, (copy) v_u_318, (copy) v_u_321, (copy) v_u_324, (copy) v_u_327
        local v352 = v_u_22.Character
        if v352 then
            v352:WaitForChild("Humanoid")
            if v_u_139 and v_u_139.Health > 0 then
                local v353 = script.Parent.GModule:FindFirstChild(p351)
                if v353 then
                    for _, v354 in pairs(v_u_101) do
                        if v354:IsA("AnimationTrack") then
                            v354:Stop()
                        end
                    end
                    v_u_101 = {}
                    local v355 = require(v353)
                    v_u_49 = nil
                    if v355.Type == "Shield" then
                        v_u_49 = v355
                        local v356 = script.Parent.GModule:FindFirstChild(v_u_35)
                        if not v356 then
                            return
                        end
                        local v357 = v_u_14:FindFirstChild(v_u_35)
                        if not v357 then
                            return
                        end
                        v_u_48 = require(v356)
                        v_u_40 = v357:Clone()
                        v_u_11.Equip:FireServer(v_u_35, 1, v_u_48, p351, v355)
                    else
                        local v358 = v_u_14:FindFirstChild(p351)
                        if not v358 then
                            return
                        end
                        v_u_48 = require(v353)
                        v_u_40 = v358:Clone()
                        v_u_11.Equip:FireServer(p351, 1, v_u_48)
                    end
                    v_u_40.PrimaryPart = v_u_40:WaitForChild("Handle")
                    for _, v359 in pairs(v353:GetChildren()) do
                        if v359:IsA("Animation") then
                            v_u_101[v359.Name] = v_u_140:LoadAnimation(v359)
                        end
                    end
                    v_u_41 = v_u_13:WaitForChild("Arms"):Clone()
                    v_u_41.Name = "Viewmodel"
                    local v360 = v352:FindFirstChild("Body Colors")
                    if v360 then
                        v360:Clone().Parent = v_u_41
                    end
                    local v361 = v352:FindFirstChild("Shirt")
                    if v361 then
                        v361:Clone().Parent = v_u_41
                    end
                    v_u_42 = Instance.new("Part", v_u_41)
                    v_u_42.Size = Vector3.new(0.1, 0.1, 0.1)
                    v_u_42.Anchored = true
                    v_u_42.CanCollide = false
                    v_u_42.Transparency = 1
                    v_u_41.PrimaryPart = v_u_42
                    v_u_45 = Instance.new("Motor6D", v_u_42)
                    v_u_45.Name = "LeftArm"
                    v_u_45.Part0 = v_u_42
                    v_u_46 = Instance.new("Motor6D", v_u_42)
                    v_u_46.Name = "RightArm"
                    v_u_46.Part0 = v_u_42
                    v_u_47 = Instance.new("Motor6D", v_u_42)
                    v_u_47.Name = "Handle"
                    v_u_41.Parent = v_u_24
                    v_u_105 = v_u_48.MainCFrame
                    v_u_106 = v_u_48.GunCFrame
                    v_u_107 = v_u_48.LArmCFrame
                    v_u_108 = v_u_48.RArmCFrame
                    if v_u_48.CrossHair then
                        v_u_4:Create(v_u_123.Up, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 0
                        }):Play()
                        v_u_4:Create(v_u_123.Down, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 0
                        }):Play()
                        v_u_4:Create(v_u_123.Left, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 0
                        }):Play()
                        v_u_4:Create(v_u_123.Right, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 0
                        }):Play()
                        if v_u_48.Bullets > 1 then
                            v_u_123.Up.Rotation = 90
                            v_u_123.Down.Rotation = 90
                            v_u_123.Left.Rotation = 90
                            v_u_123.Right.Rotation = 90
                        else
                            v_u_123.Up.Rotation = 0
                            v_u_123.Down.Rotation = 0
                            v_u_123.Left.Rotation = 0
                            v_u_123.Right.Rotation = 0
                        end
                    else
                        v_u_4:Create(v_u_123.Up, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 1
                        }):Play()
                        v_u_4:Create(v_u_123.Down, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 1
                        }):Play()
                        v_u_4:Create(v_u_123.Left, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 1
                        }):Play()
                        v_u_4:Create(v_u_123.Right, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["BackgroundTransparency"] = 1
                        }):Play()
                    end
                    if v_u_48.CenterDot then
                        v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["ImageTransparency"] = 0
                        }):Play()
                    else
                        v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
                            ["ImageTransparency"] = 1
                        }):Play()
                    end
                    v_u_43 = v_u_41:WaitForChild("Left Arm")
                    v_u_45.Part1 = v_u_43
                    v_u_45.C0 = CFrame.new()
                    v_u_45.C1 = CFrame.new(1, -1, -5) * CFrame.Angles(0, 0, 0):inverse()
                    v_u_44 = v_u_41:WaitForChild("Right Arm")
                    v_u_46.Part1 = v_u_44
                    v_u_46.C0 = CFrame.new()
                    v_u_46.C1 = CFrame.new(-1, -1, -5) * CFrame.Angles(0, 0, 0):inverse()
                    v_u_47.Part0 = v_u_44
                    v_u_43.Anchored = false
                    v_u_44.Anchored = false
                    v_u_104.ZoomValue = v_u_48.Zoom
                    loadAttachment(v_u_40)
                    local v362 = v_u_48.MinSpread * v_u_104.MinSpread
                    local v363 = v_u_48.MaxSpread * v_u_104.MaxSpread
                    v_u_55 = math.min(v362, v363)
                    local v364 = v_u_48.MinRecoilPower * v_u_104.MinRecoilPower
                    local v365 = v_u_48.MaxRecoilPower * v_u_104.MaxRecoilPower
                    v_u_56 = math.min(v364, v365)
                    v_u_31.ApplySkin(v_u_40, v_u_48.SkinTable)
                    if v_u_49 then
                        local v366 = v_u_14:FindFirstChild(v_u_34)
                        if not v366 then
                            return
                        end
                        local v367 = v366:Clone()
                        v367.PrimaryPart = v367:WaitForChild("Handle")
                        v_u_104.MinSpread = v_u_104.MinSpread * 3
                        v_u_104.WalkMult = v_u_104.WalkMult * 2
                        local v368 = v_u_48.MinSpread * v_u_104.MinSpread
                        local v369 = v_u_48.MaxSpread * v_u_104.MaxSpread
                        v_u_55 = math.min(v368, v369)
                        v_u_107 = v_u_49.LArmCFrame
                        v_u_108 = v_u_49.RArmCFrame
                        local v370 = Instance.new("Motor6D", v_u_42)
                        v370.Part0 = v_u_43
                        v370.Part1 = v367:WaitForChild("Handle")
                        for _, v371 in pairs(v367:GetChildren()) do
                            if v371:IsA("BasePart") and v371.Name ~= "Handle" then
                                v_u_29.Weld(v371, v367:WaitForChild("Handle"))
                            end
                        end
                        for _, v372 in pairs(v367:GetChildren()) do
                            if v372:IsA("BasePart") then
                                v372.Anchored = false
                                v372.CanCollide = false
                            end
                        end
                        v_u_31.ApplySkin(v367, v_u_49.SkinTable)
                        v370.C1 = v_u_49.GunCFrame
                        v367.Parent = v_u_41
                    end
                    UpdateGui()
                    for _, v373 in pairs(v_u_40:GetChildren()) do
                        if v373:IsA("BasePart") and v373.Name ~= "Handle" then
                            if not string.match(v373.Name, "Bolt") and (v373.Name ~= "Lid" and not string.match(v373.Name, "Slide")) then
                                v_u_29.Weld(v_u_40:WaitForChild("Handle"), v373)
                            end
                            if string.match(v373.Name, "Bolt") or string.match(v373.Name, "Slide") then
                                v_u_29.WeldComplex(v_u_40:WaitForChild("Handle"), v373, v373.Name)
                            end
                            if v373.Name == "Lid" then
                                if v_u_40:FindFirstChild("LidHinge") then
                                    v_u_29.Weld(v373, v_u_40:WaitForChild("LidHinge"))
                                else
                                    v_u_29.Weld(v373, v_u_40:WaitForChild("Handle"))
                                end
                            end
                        end
                    end
                    for _, v374 in pairs(v_u_40:GetDescendants()) do
                        if v374:IsA("BasePart") then
                            if v374.Parent:IsA("Folder") or v374.Parent:IsA("Model") and v374.Parent ~= v_u_40 then
                                v_u_29.Weld(v_u_40:WaitForChild("Handle"), v374)
                            end
                            v374.Anchored = false
                            v374.CanCollide = false
                        end
                    end
                    v_u_47.Part1 = v_u_40:WaitForChild("Handle")
                    v_u_47.C1 = v_u_106
                    v_u_40.Parent = v_u_41
                    if v_u_48.AmmoInGun <= 0 and (v_u_48.Type == "Gun" and v_u_48.SlideLock) then
                        for _, v375 in pairs(v_u_40.Handle:GetChildren()) do
                            if v375:IsA("Motor6D") and string.match(v375.Name, "Slide") then
                                v375.C0 = v_u_48.SlideEx:inverse()
                            end
                        end
                    end
                    EquipAnim()
                    if v_u_48 and (v_u_48.Type ~= "Grenade" and v_u_48.Type ~= "Placeable") then
                        RunCheck()
                    end
                    if v_u_48 and v_u_48.OnEquip then
                        v_u_48.OnEquip(v_u_22)
                    end
                    v_u_2:BindAction("Fire", v_u_318, true, Enum.UserInputType.MouseButton1)
                    v_u_2:BindAction("ADS", v_u_321, true, Enum.UserInputType.MouseButton2)
                    v_u_2:BindAction("Reload", v_u_324, true, Enum.KeyCode.R)
                    v_u_2:BindAction("Melee", v_u_327, true, Enum.KeyCode.V)
                end
            else
                return
            end
        else
            return
        end
    end
    function unset()
        -- upvalues: (copy) v_u_11, (ref) v_u_40, (copy) v_u_2, (ref) v_u_78, (ref) v_u_75, (copy) v_u_223, (copy) v_u_1, (copy) v_u_62, (copy) v_u_4, (copy) v_u_24, (copy) v_u_113, (copy) v_u_60, (copy) v_u_123, (ref) v_u_101, (ref) v_u_48, (copy) v_u_22, (ref) v_u_41, (ref) v_u_43, (ref) v_u_44, (ref) v_u_45, (ref) v_u_46, (ref) v_u_86, (ref) v_u_87, (ref) v_u_90, (ref) v_u_91, (ref) v_u_92, (ref) v_u_93, (ref) v_u_94, (ref) v_u_55, (ref) v_u_56, (ref) v_u_88, (ref) v_u_89, (ref) v_u_82, (ref) v_u_54
        UnsetCamera()
        UnsetDrone()
        v_u_11.Equip:FireServer(v_u_40.Name, 2, nil)
        v_u_2:UnbindAction("Fire")
        v_u_2:UnbindAction("ADS")
        v_u_2:UnbindAction("Reload")
        v_u_2:UnbindAction("Melee")
        v_u_78 = false
        v_u_75 = false
        v_u_223(v_u_75)
        v_u_1.MouseDeltaSensitivity = v_u_62
        v_u_4:Create(v_u_24, v_u_113, {
            ["FieldOfView"] = v_u_60
        }):Play()
        v_u_4:Create(v_u_123.Up, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
            ["BackgroundTransparency"] = 1
        }):Play()
        v_u_4:Create(v_u_123.Down, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
            ["BackgroundTransparency"] = 1
        }):Play()
        v_u_4:Create(v_u_123.Left, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
            ["BackgroundTransparency"] = 1
        }):Play()
        v_u_4:Create(v_u_123.Right, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
            ["BackgroundTransparency"] = 1
        }):Play()
        v_u_4:Create(v_u_123.Center, TweenInfo.new(0.2, Enum.EasingStyle.Linear), {
            ["ImageTransparency"] = 1
        }):Play()
        for _, v376 in pairs(v_u_101) do
            v376:Stop()
        end
        if v_u_48 and v_u_48.OnUnequip then
            v_u_48.OnUnequip(v_u_22)
        end
        if v_u_41 then
            UnEquipAnim()
            v_u_41:Destroy()
            v_u_41 = nil
            v_u_40 = nil
            v_u_43 = nil
            v_u_44 = nil
            v_u_45 = nil
            v_u_46 = nil
            v_u_48 = nil
            v_u_86 = nil
            v_u_87 = nil
            v_u_90 = nil
            v_u_91 = nil
            v_u_92 = false
            v_u_93 = 0
            v_u_94 = nil
            v_u_55 = nil
            v_u_56 = nil
            v_u_88 = false
            v_u_89 = false
            v_u_82 = false
            resetMods()
            v_u_54 = 0
            v_u_11.SVLaser:FireServer(nil, nil, 2, nil, false)
        end
    end
    function Recoil()
        -- upvalues: (copy) v_u_23, (ref) v_u_48, (copy) v_u_104, (copy) v_u_125, (ref) v_u_75, (copy) v_u_124, (ref) v_u_56, (ref) v_u_111
        local v377 = v_u_23:FindFirstChild("Adrenaline") and 2 or 1
        local v378 = math.random(v_u_48.camRecoil.camRecoilUp[1], v_u_48.camRecoil.camRecoilUp[2]) / 2 * v_u_104.camRecoilMod.RecoilUp
        local v379 = math.random(v_u_48.camRecoil.camRecoilLeft[1], v_u_48.camRecoil.camRecoilLeft[2]) * v_u_104.camRecoilMod.RecoilLeft
        local v380 = math.random(v_u_48.camRecoil.camRecoilRight[1], v_u_48.camRecoil.camRecoilRight[2]) * v_u_104.camRecoilMod.RecoilRight
        local v381 = math.random(-v380, v379) / 2
        local v382 = math.random(v_u_48.camRecoil.camRecoilTilt[1], v_u_48.camRecoil.camRecoilTilt[2]) / 2 * v_u_104.camRecoilMod.RecoilTilt
        local v383 = v378 * RAND(1, 1, 0.1)
        local v_u_384 = math.rad(v383) / v377
        local v385 = v381 * RAND(-1, 1, 0.1)
        local v_u_386 = math.rad(v385) / v377
        local v387 = v382 * RAND(-1, 1, 0.1)
        local v388 = math.rad(v387) / v377
        local v389 = math.random(v_u_48.gunRecoil.gunRecoilUp[1], v_u_48.gunRecoil.gunRecoilUp[2]) / 10 * v_u_104.gunRecoilMod.RecoilUp / v377
        local v390 = math.random(-1, 1) * math.random(v_u_48.gunRecoil.gunRecoilTilt[1], v_u_48.gunRecoil.gunRecoilTilt[2]) / 10 * v_u_104.gunRecoilMod.RecoilTilt / v377
        local v391 = math.random(v_u_48.gunRecoil.gunRecoilLeft[1], v_u_48.gunRecoil.gunRecoilLeft[2]) * v_u_104.gunRecoilMod.RecoilLeft / v377
        local v392 = math.random(v_u_48.gunRecoil.gunRecoilRight[1], v_u_48.gunRecoil.gunRecoilRight[2]) * v_u_104.gunRecoilMod.RecoilRight / v377
        local v393 = math.random(-v392, v391) / 10
        local v394 = v_u_48.AimRecoilReduction * v_u_104.AimRM
        v_u_125:shove((Vector3.new(v_u_384, v_u_386, v388)))
        task.spawn(function()
            -- upvalues: (ref) v_u_125, (copy) v_u_384, (copy) v_u_386
            wait(0.1)
            local v395 = v_u_125
            local v396 = -v_u_384
            local v397 = -v_u_386
            v395:shove((Vector3.new(v396, v397, 0)))
        end)
        if v_u_75 then
            local v398 = v_u_124
            local v399 = v389 * v_u_56 / v394
            local v400 = math.rad(v399)
            local v401 = v393 * v_u_56 / v394
            local v402 = math.rad(v401)
            local v403 = v390 / v394
            local v404 = math.rad(v403)
            v398:shove((Vector3.new(v400, v402, v404)))
            local v405 = v_u_111 * CFrame.new(0, 0, 0.1)
            local v406 = CFrame.Angles
            local v407 = v389 * v_u_56 / v394
            local v408 = math.rad(v407)
            local v409 = v393 * v_u_56 / v394
            local v410 = math.rad(v409)
            local v411 = v390 * v_u_56 / v394
            v_u_111 = v405 * v406(v408, v410, (math.rad(v411)))
        else
            local v412 = v_u_124
            local v413 = v389 * v_u_56
            local v414 = math.rad(v413)
            local v415 = v393 * v_u_56
            local v416 = math.rad(v415)
            local v417 = math.rad(v390)
            v412:shove((Vector3.new(v414, v416, v417)))
            local v418 = v_u_111 * CFrame.new(0, -0.05, 0.1)
            local v419 = CFrame.Angles
            local v420 = v389 * v_u_56
            local v421 = math.rad(v420)
            local v422 = v393 * v_u_56
            local v423 = math.rad(v422)
            local v424 = v390 * v_u_56
            v_u_111 = v418 * v419(v421, v423, (math.rad(v424)))
        end
    end
    function CheckForHumanoid(p425)
        local v426 = nil
        local v427
        if p425 and (p425.Parent:FindFirstChildOfClass("Humanoid") or p425.Parent.Parent:FindFirstChildOfClass("Humanoid")) then
            v427 = true
            if p425.Parent:FindFirstChildOfClass("Humanoid") then
                return v427, p425.Parent:FindFirstChildOfClass("Humanoid")
            end
            if p425.Parent.Parent:FindFirstChildOfClass("Humanoid") then
                return v427, p425.Parent.Parent:FindFirstChildOfClass("Humanoid")
            end
        else
            v427 = false
        end
        return v427, v426
    end
    function BulletRaycast(p428, p429, p430)
        -- upvalues: (copy) v_u_24, (copy) v_u_114
        local v431 = p428 or v_u_24.CFrame.Position
        local v432 = p429 or v_u_24.CFrame.LookVector
        local v433 = { v_u_114 }
        if p430 then
            table.insert(v433, p430)
        end
        local v434 = RaycastParams.new()
        v434.FilterDescendantsInstances = v433
        v434.FilterType = Enum.RaycastFilterType.Exclude
        v434.CollisionGroup = "BulletCast"
        return workspace:Raycast(v431, v432 * 5000, v434)
    end
    function BulletDamage(p435, p436, p437)
        -- upvalues: (ref) v_u_48, (copy) v_u_58, (copy) v_u_22, (copy) v_u_11, (copy) v_u_104
        if p435 then
            local v438 = p436 or 0
            local v439 = p437 or false
            local v440, v441 = CheckForHumanoid(p435)
            if v440 == true and (v441.Health > 0 and (v440 == true and (v441.Health > 0 and v_u_48))) then
                local v442 = v_u_58 .. "-" .. v_u_22.UserId
                if p435.Name == "Head" or (p435.Parent.Name == "Top" or (p435.Parent.Name == "Headset" or (p435.Parent.Name == "Olho" or (p435.Parent.Name == "Face" or p435.Parent.Name == "Numero")))) then
                    v_u_11.Damage:FireServer(v441, v438, 1, v_u_48, v_u_104, nil, nil, v442, v439)
                    return
                end
                if p435.Name == "Torso" or (p435.Name == "UpperTorso" or (p435.Name == "LowerTorso" or (p435.Parent.Name == "Chest" or (p435.Parent.Name == "Waist" or (p435.Name == "Right Arm" or (p435.Name == "Left Arm" or (p435.Name == "RightUpperArm" or (p435.Name == "RightLowerArm" or (p435.Name == "RightHand" or (p435.Name == "LeftUpperArm" or (p435.Name == "LeftLowerArm" or p435.Name == "LeftHand"))))))))))) then
                    v_u_11.Damage:FireServer(v441, v438, 2, v_u_48, v_u_104, nil, nil, v442, v439)
                    return
                end
                v_u_11.Damage:FireServer(v441, v438, 3, v_u_48, v_u_104, nil, nil, v442, v439)
            end
        end
    end
    function Wallbang(p443, p444, p445)
        -- upvalues: (copy) v_u_9, (copy) v_u_24, (copy) v_u_5, (copy) v_u_18, (copy) v_u_114, (copy) v_u_27, (ref) v_u_48, (copy) v_u_11
        if p445 and p445.Parent then
            if p445:IsDescendantOf(v_u_9.Doors) or p445:IsDescendantOf(v_u_9.Breach) then
                if p445.Material == Enum.Material.Wood or p445.Material == Enum.Material.WoodPlanks then
                    local v446 = p443 or v_u_24.CFrame.Position
                    local v447 = p444 or v_u_24.CFrame.LookVector
                    local v448 = BulletRaycast(v446, v447, p445.Parent)
                    local v449 = Instance.new("Attachment", workspace.Terrain)
                    v_u_5:AddItem(v449, 1)
                    v449.WorldPosition = v446
                    local v450 = Instance.new("Attachment", workspace.Terrain)
                    v_u_5:AddItem(v450, 1)
                    local v451 = v_u_18.BulletTrail:Clone()
                    v451.Parent = v449
                    v451.Attachment0 = v449
                    v451.Attachment1 = v450
                    if v448 then
                        local v452 = v448.Instance
                        if v452 and v452.Parent:IsA("Accessory") or v452.Parent:IsA("Hat") then
                            for _, v453 in pairs(game.Players:GetPlayers()) do
                                if v453.Character then
                                    for _, v454 in pairs(v453.Character:GetChildren()) do
                                        if v454:IsA("Accessory") then
                                            local v455 = v_u_114
                                            table.insert(v455, v454)
                                        end
                                    end
                                end
                            end
                            return new_bullet(true)
                        elseif v452 and v452.Name == "Ignorable" or (v452.Name == "Glass" or (v452.Name == "Ignore" or (v452.Parent.Name == "Top" or (v452.Parent.Name == "Helmet" or (v452.Parent.Name == "Up" or (v452.Parent.Name == "Down" or (v452.Parent.Name == "Face" or (v452.Parent.Name == "Olho" or (v452.Parent.Name == "Headset" or (v452.Parent.Name == "Numero" or (v452.Parent.Name == "Vest" or (v452.Parent.Name == "Chest" or (v452.Parent.Name == "Waist" or (v452.Parent.Name == "Back" or (v452.Parent.Name == "Belt" or (v452.Parent.Name == "Leg1" or (v452.Parent.Name == "Leg2" or (v452.Parent.Name == "Arm1" or v452.Parent.Name == "Arm2")))))))))))))))))) then
                            local v456 = v_u_114
                            table.insert(v456, v452)
                            return Wallbang(p443, p444, p445)
                        elseif v452 and v452.Parent.Name == "Top" or (v452.Parent.Name == "Helmet" or (v452.Parent.Name == "Up" or (v452.Parent.Name == "Down" or (v452.Parent.Name == "Face" or (v452.Parent.Name == "Olho" or (v452.Parent.Name == "Headset" or (v452.Parent.Name == "Numero" or (v452.Parent.Name == "Vest" or (v452.Parent.Name == "Chest" or (v452.Parent.Name == "Waist" or (v452.Parent.Name == "Back" or (v452.Parent.Name == "Belt" or (v452.Parent.Name == "Leg1" or (v452.Parent.Name == "Leg2" or (v452.Parent.Name == "Arm1" or v452.Parent.Name == "Arm2"))))))))))))))) then
                            local v457 = v_u_114
                            local v458 = v452.Parent
                            table.insert(v457, v458)
                            return Wallbang(p443, p444, p445)
                        elseif v452 and (v452.Transparency >= 1 or v452.CanCollide == false) and (v452.Name ~= "Head" and (v452.Name ~= "Right Arm" and (v452.Name ~= "Left Arm" and (v452.Name ~= "Right Leg" and (v452.Name ~= "Left Leg" and (v452.Name ~= "UpperTorso" and (v452.Name ~= "LowerTorso" and (v452.Name ~= "RightUpperArm" and (v452.Name ~= "RightLowerArm" and (v452.Name ~= "RightHand" and (v452.Name ~= "LeftUpperArm" and (v452.Name ~= "LeftLowerArm" and (v452.Name ~= "LeftHand" and (v452.Name ~= "RightUpperLeg" and (v452.Name ~= "RightLowerLeg" and (v452.Name ~= "RightFoot" and (v452.Name ~= "LeftUpperLeg" and (v452.Name ~= "LeftLowerLeg" and (v452.Name ~= "LeftFoot" and (v452.Name ~= "Armor" and v452.Name ~= "EShield")))))))))))))))))))) then
                            local v459 = v_u_114
                            table.insert(v459, v452)
                            return Wallbang(p443, p444, p445)
                        else
                            local v460 = (v448.Position - v_u_24.CFrame.Position).Magnitude
                            v_u_27.HitEffect(v_u_114, v448.Position, v448.Instance, v448.Normal, v448.Material, v_u_48)
                            v_u_11.HitEffect:FireServer(v448.Position, v448.Instance, v448.Normal, v448.Material, v_u_48)
                            v_u_11.ReplicateTracer:FireServer(p443, v448.Position, true)
                            v450.WorldPosition = v448.Position
                            if v452.Name ~= "Armor" then
                                BulletDamage(v448.Instance, v460, true)
                            end
                        end
                    else
                        v450.WorldPosition = v446 + p444 * 1000
                        v_u_11.ReplicateTracer:FireServer(p443, v446 + p444 * 1000, true)
                        return
                    end
                else
                    return
                end
            else
                return
            end
        else
            return
        end
    end
    function new_bullet(p461)
        -- upvalues: (ref) v_u_48, (copy) v_u_104, (ref) v_u_99, (ref) v_u_75, (ref) v_u_55, (ref) v_u_72, (copy) v_u_24, (ref) v_u_40, (copy) v_u_114, (ref) v_u_88, (copy) v_u_18, (copy) v_u_11, (copy) v_u_5, (copy) v_u_27
        local v462 = v_u_48.WalkMult * v_u_104.WalkMult
        local v463 = 10 * (v_u_99.X > 0.975 and 1 or 0) * v_u_48.AimSpreadReduction
        local v464 = math.max(10, v463)
        local v465
        if v_u_75 and v_u_48.Bullets <= 1 then
            local v466 = CFrame.Angles
            local v467 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / v464
            local v468 = math.rad(v467)
            local v469 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / v464
            local v470 = math.rad(v469)
            local v471 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / v464
            v465 = v466(v468, v470, (math.rad(v471)))
        else
            local v472 = CFrame.Angles
            local v473 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / 10
            local v474 = math.rad(v473)
            local v475 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / 10
            local v476 = math.rad(v475)
            local v477 = RAND(-v_u_55 - v_u_72 / 1 * v462, v_u_55 + v_u_72 / 1 * v462) / 10
            v465 = v472(v474, v476, (math.rad(v477)))
        end
        local v478 = v_u_24.CFrame.Position
        local v479 = v465 * v_u_40.Handle.Muzzle.WorldCFrame.LookVector * 5000
        local v480 = BulletRaycast(v478, v479, nil)
        if v480 then
            local v481 = v480.Instance
            if v481 and v481.Parent:IsA("Accessory") or v481.Parent:IsA("Hat") then
                for _, v482 in pairs(game.Players:GetPlayers()) do
                    if v482.Character then
                        for _, v483 in pairs(v482.Character:GetChildren()) do
                            if v483:IsA("Accessory") then
                                local v484 = v_u_114
                                table.insert(v484, v483)
                            end
                        end
                    end
                end
                return new_bullet(p461)
            elseif v481 and v481.Name == "Ignorable" or (v481.Name == "Glass" or (v481.Name == "Ignore" or (v481.Parent.Name == "Top" or (v481.Parent.Name == "Helmet" or (v481.Parent.Name == "Up" or (v481.Parent.Name == "Down" or (v481.Parent.Name == "Face" or (v481.Parent.Name == "Olho" or (v481.Parent.Name == "Headset" or (v481.Parent.Name == "Numero" or (v481.Parent.Name == "Vest" or (v481.Parent.Name == "Chest" or (v481.Parent.Name == "Waist" or (v481.Parent.Name == "Back" or (v481.Parent.Name == "Belt" or (v481.Parent.Name == "Leg1" or (v481.Parent.Name == "Leg2" or (v481.Parent.Name == "Arm1" or v481.Parent.Name == "Arm2")))))))))))))))))) then
                local v485 = v_u_114
                table.insert(v485, v481)
                return new_bullet(p461)
            elseif v481 and v481.Parent.Name == "Top" or (v481.Parent.Name == "Helmet" or (v481.Parent.Name == "Up" or (v481.Parent.Name == "Down" or (v481.Parent.Name == "Face" or (v481.Parent.Name == "Olho" or (v481.Parent.Name == "Headset" or (v481.Parent.Name == "Numero" or (v481.Parent.Name == "Vest" or (v481.Parent.Name == "Chest" or (v481.Parent.Name == "Waist" or (v481.Parent.Name == "Back" or (v481.Parent.Name == "Belt" or (v481.Parent.Name == "Leg1" or (v481.Parent.Name == "Leg2" or (v481.Parent.Name == "Arm1" or v481.Parent.Name == "Arm2"))))))))))))))) then
                local v486 = v_u_114
                local v487 = v481.Parent
                table.insert(v486, v487)
                return new_bullet(p461)
            elseif v481 and (v481.Transparency >= 1 or v481.CanCollide == false) and (v481.Name ~= "Head" and (v481.Name ~= "Right Arm" and (v481.Name ~= "Left Arm" and (v481.Name ~= "Right Leg" and (v481.Name ~= "Left Leg" and (v481.Name ~= "UpperTorso" and (v481.Name ~= "LowerTorso" and (v481.Name ~= "RightUpperArm" and (v481.Name ~= "RightLowerArm" and (v481.Name ~= "RightHand" and (v481.Name ~= "LeftUpperArm" and (v481.Name ~= "LeftLowerArm" and (v481.Name ~= "LeftHand" and (v481.Name ~= "RightUpperLeg" and (v481.Name ~= "RightLowerLeg" and (v481.Name ~= "RightFoot" and (v481.Name ~= "LeftUpperLeg" and (v481.Name ~= "LeftLowerLeg" and (v481.Name ~= "LeftFoot" and (v481.Name ~= "Armor" and v481.Name ~= "EShield")))))))))))))))))))) then
                local v488 = v_u_114
                table.insert(v488, v481)
                return new_bullet(p461)
            else
                if not v_u_88 then
                    local v489 = Instance.new("Attachment", workspace.Terrain)
                    local v490 = Instance.new("Attachment", workspace.Terrain)
                    v489.WorldPosition = v_u_40.Handle.Muzzle.WorldPosition
                    local v491 = v_u_18.BulletTrail:Clone()
                    v491.Parent = v489
                    v491.Attachment0 = v489
                    v491.Attachment1 = v490
                    v490.WorldPosition = v480.Position
                    v_u_11.ReplicateTracer:FireServer(v_u_40.Handle.Muzzle.WorldPosition, v480.Position, false)
                    v_u_5:AddItem(v490, 0.25)
                    v_u_5:AddItem(v489, 0.25)
                end
                v_u_27.HitEffect(v_u_114, v480.Position, v480.Instance, v480.Normal, v480.Material, v_u_48)
                v_u_11.HitEffect:FireServer(v480.Position, v480.Instance, v480.Normal, v480.Material, v_u_48)
                if v480.Instance.Name ~= "Armor" then
                    Wallbang(v480.Position, v479, v480.Instance)
                    BulletDamage(v480.Instance, 0, p461)
                end
            end
        else
            if not v_u_88 then
                local v492 = Instance.new("Attachment", workspace.Terrain)
                local v493 = Instance.new("Attachment", workspace.Terrain)
                v492.WorldPosition = v_u_40.Handle.Muzzle.WorldPosition
                local v494 = v_u_18.BulletTrail:Clone()
                v494.Parent = v492
                v494.Attachment0 = v492
                v494.Attachment1 = v493
                v493.WorldPosition = v_u_24.CFrame.Position + v479
                v_u_11.ReplicateTracer:FireServer(v_u_40.Handle.Muzzle.WorldPosition, v_u_24.CFrame.Position + v479, false)
                v_u_5:AddItem(v493, 0.25)
                v_u_5:AddItem(v492, 0.25)
            end
            return
        end
    end
    function meleeCast()
        -- upvalues: (ref) v_u_84, (copy) v_u_30, (ref) v_u_48, (ref) v_u_49, (copy) v_u_24, (copy) v_u_115, (copy) v_u_27, (copy) v_u_11, (copy) v_u_58, (copy) v_u_22, (copy) v_u_104
        if not (v_u_84 or v_u_30.InDrone) then
            if not v_u_48 then
                warn("WeaponData Not Found")
                return
            end
            local v495 = v_u_49 or v_u_48
            local v496 = v_u_24.CFrame.Position
            local v497 = v_u_24.CFrame.LookVector
            local v498 = RaycastParams.new()
            v498.FilterDescendantsInstances = v_u_115
            v498.FilterType = Enum.RaycastFilterType.Exclude
            v498.IgnoreWater = true
            local v499 = workspace:Raycast(v496, v497 * 8, v498)
            if not v499 then
                return
            end
            local v500 = v499.Instance
            if v500 and v500.Parent:IsA("Accessory") then
                local v501 = v_u_115
                local v502 = v500.Parent
                table.insert(v501, v502)
                for _, v503 in pairs(game.Players:GetPlayers()) do
                    if v503.Character then
                        for _, v504 in pairs(v503.Character:GetChildren()) do
                            if v504:IsA("Accessory") then
                                local v505 = v_u_115
                                table.insert(v505, v504)
                            end
                        end
                    end
                end
                return meleeCast()
            end
            if v500 and v500.Name == "Ignorable" or (v500.Name == "Glass" or (v500.Name == "Ignore" or (v500.Parent.Name == "Top" or (v500.Parent.Name == "Helmet" or (v500.Parent.Name == "Up" or (v500.Parent.Name == "Down" or (v500.Parent.Name == "Face" or (v500.Parent.Name == "Olho" or (v500.Parent.Name == "Headset" or (v500.Parent.Name == "Numero" or (v500.Parent.Name == "Vest" or (v500.Parent.Name == "Chest" or (v500.Parent.Name == "Waist" or (v500.Parent.Name == "Back" or (v500.Parent.Name == "Belt" or (v500.Parent.Name == "Leg1" or (v500.Parent.Name == "Leg2" or (v500.Parent.Name == "Arm1" or v500.Parent.Name == "Arm2")))))))))))))))))) then
                local v506 = v_u_115
                table.insert(v506, v500)
                return meleeCast()
            end
            if v500 and v500.Parent.Name == "Top" or (v500.Parent.Name == "Helmet" or (v500.Parent.Name == "Up" or (v500.Parent.Name == "Down" or (v500.Parent.Name == "Face" or (v500.Parent.Name == "Olho" or (v500.Parent.Name == "Headset" or (v500.Parent.Name == "Numero" or (v500.Parent.Name == "Vest" or (v500.Parent.Name == "Chest" or (v500.Parent.Name == "Waist" or (v500.Parent.Name == "Back" or (v500.Parent.Name == "Belt" or (v500.Parent.Name == "Leg1" or (v500.Parent.Name == "Leg2" or (v500.Parent.Name == "Arm1" or v500.Parent.Name == "Arm2"))))))))))))))) then
                local v507 = v_u_115
                local v508 = v500.Parent
                table.insert(v507, v508)
                return meleeCast()
            end
            if v500 and (v500.Transparency >= 1 or v500.CanCollide == false) and (v500.Name ~= "Head" and (v500.Name ~= "Right Arm" and (v500.Name ~= "Left Arm" and (v500.Name ~= "Right Leg" and (v500.Name ~= "Left Leg" and (v500.Name ~= "UpperTorso" and (v500.Name ~= "LowerTorso" and (v500.Name ~= "RightUpperArm" and (v500.Name ~= "RightLowerArm" and (v500.Name ~= "RightHand" and (v500.Name ~= "LeftUpperArm" and (v500.Name ~= "LeftLowerArm" and (v500.Name ~= "LeftHand" and (v500.Name ~= "RightUpperLeg" and (v500.Name ~= "RightLowerLeg" and (v500.Name ~= "RightFoot" and (v500.Name ~= "LeftUpperLeg" and (v500.Name ~= "LeftLowerLeg" and (v500.Name ~= "LeftFoot" and (v500.Name ~= "Armor" and (v500.Name ~= "EShield" and v500.Name ~= "MeleeShield"))))))))))))))))))))) then
                local v509 = v_u_115
                table.insert(v509, v500)
                return meleeCast()
            end
            v_u_27.HitEffect(v_u_115, v499.Position, v499.Instance, v499.Normal, v499.Material, v495)
            v_u_11.HitEffect:FireServer(v499.Position, v499.Instance, v499.Normal, v499.Material, v495)
            local v510, v511 = CheckForHumanoid(v499.Instance)
            local v512 = v499.Instance
            if v512.Name == "Armor" then
                return
            end
            if not v510 or v511.Health <= 0 then
                return
            end
            local v513 = v_u_58 .. "-" .. v_u_22.UserId
            if v512.Name == "Head" or (v512.Parent.Name == "Top" or (v512.Parent.Name == "Headset" or (v512.Parent.Name == "Olho" or (v512.Parent.Name == "Face" or v512.Parent.Name == "Numero")))) then
                v_u_11.Damage:FireServer(v511, 0, 1, v495, v_u_104, nil, nil, v513)
                return
            end
            if v512.Name == "Torso" or (v512.Name == "UpperTorso" or (v512.Name == "LowerTorso" or (v512.Parent.Name == "Chest" or (v512.Parent.Name == "Waist" or (v512.Name == "RightUpperArm" or (v512.Name == "RightLowerArm" or (v512.Name == "RightHand" or (v512.Name == "LeftUpperArm" or (v512.Name == "LeftLowerArm" or v512.Name == "LeftHand"))))))))) then
                v_u_11.Damage:FireServer(v511, 0, 2, v495, v_u_104, nil, nil, v513)
                return
            end
            v_u_11.Damage:FireServer(v511, 0, 3, v495, v_u_104, nil, nil, v513)
        end
    end
    function UpdateGui()
        -- upvalues: (ref) v_u_120, (ref) v_u_48, (ref) v_u_38, (ref) v_u_39
        if v_u_120 then
            local v514 = v_u_120.HealthHud.AmmoHud
            local v515 = v_u_120.HealthHud.Ut
            local v516 = v_u_120.HealthHud.Gr
            v514.gun.Text = v_u_48.gunName
            if v_u_48.Type == "Gun" then
                v514.Ammo.Text = v_u_48.AmmoInGun
                v514.Store.Text = v_u_48.StoredAmmo
            else
                v514.Ammo.Text = "---"
                v514.Store.Text = "---"
            end
            v515.qnt.Text = v_u_38
            v516.qnt.Text = v_u_39
        end
    end
    function Melee()
        -- upvalues: (ref) v_u_76, (copy) v_u_139, (ref) v_u_48, (ref) v_u_49, (ref) v_u_75, (ref) v_u_41, (ref) v_u_33, (ref) v_u_34, (ref) v_u_35
        if v_u_76 or v_u_139.Health <= 0 then
            return
        elseif v_u_48 and v_u_48.Type == "Melee" or v_u_49 then
            if not v_u_75 then
                v_u_76 = true
                task.spawn(function()
                    -- upvalues: (ref) v_u_48
                    local v517 = v_u_48.Bullets
                    for _ = 1, math.max(v517, 1) do
                        meleeCast()
                        task.wait(0.016666666666666666)
                    end
                end)
                meleeAttack()
                RunCheck()
                v_u_76 = false
            end
        else
            if v_u_41 then
                unset()
            end
            setup("Knife")
            v_u_76 = true
            meleeCast()
            meleeAttack()
            unset()
            v_u_76 = false
            if v_u_33 == 1 then
                setup(v_u_34)
                return
            elseif v_u_33 == 2 then
                setup(v_u_35)
            else
                setup(v_u_34)
            end
        end
    end
    function Gadget()
        -- upvalues: (copy) v_u_139, (ref) v_u_74, (ref) v_u_48, (copy) v_u_22, (ref) v_u_41, (ref) v_u_32, (ref) v_u_38, (ref) v_u_39, (ref) v_u_33, (ref) v_u_34, (ref) v_u_35
        if v_u_139.Health <= 0 then
            return
        elseif not v_u_74 then
            if v_u_48 and v_u_48.OnActivate then
                Recoil()
                v_u_48.OnActivate(v_u_22, v_u_41, v_u_32)
                if v_u_32 == 3 then
                    v_u_38 = v_u_48.Ammo
                elseif v_u_32 == 4 then
                    v_u_39 = v_u_48.Ammo
                end
            end
            unset()
            if v_u_33 == 1 then
                v_u_32 = 1
                setup(v_u_34)
            elseif v_u_33 == 2 then
                v_u_32 = 2
                setup(v_u_35)
            else
                v_u_32 = 1
                v_u_33 = 1
                setup(v_u_34)
            end
            UpdateGui()
        end
    end
    function Placeable()
        -- upvalues: (ref) v_u_48, (copy) v_u_139, (ref) v_u_95, (copy) v_u_11, (copy) v_u_24, (ref) v_u_32, (ref) v_u_38, (ref) v_u_39, (ref) v_u_33, (ref) v_u_34, (ref) v_u_35
        if v_u_48.Type == "Placeable" then
            if v_u_139.Health > 0 then
                v_u_95 = true
                v_u_11.Grenade:FireServer(v_u_48, v_u_24.CFrame, v_u_24.CFrame.LookVector, true, v_u_32)
                if v_u_32 == 3 then
                    v_u_38 = v_u_38 - 1
                elseif v_u_32 == 4 then
                    v_u_39 = v_u_39 - 1
                end
                task.wait(0.2)
                unset()
                if v_u_33 == 1 then
                    v_u_32 = 1
                    setup(v_u_34)
                elseif v_u_33 == 2 then
                    v_u_32 = 2
                    setup(v_u_35)
                else
                    v_u_32 = 1
                    v_u_33 = 1
                    setup(v_u_34)
                end
                UpdateGui()
                v_u_95 = false
            end
        else
            return
        end
    end
    function Grenade()
        -- upvalues: (copy) v_u_139, (ref) v_u_95, (ref) v_u_96
        if v_u_139.Health > 0 then
            v_u_95 = true
            repeat
                wait()
            until not v_u_96
            TossGrenade()
        end
    end
    function TossGrenade()
        -- upvalues: (copy) v_u_139, (ref) v_u_95, (copy) v_u_11, (ref) v_u_48, (copy) v_u_24, (ref) v_u_32, (ref) v_u_38, (ref) v_u_39, (ref) v_u_33, (ref) v_u_34, (ref) v_u_35
        if v_u_139.Health > 0 and v_u_95 then
            GrenadeThrow()
            v_u_11.Grenade:FireServer(v_u_48, v_u_24.CFrame, v_u_24.CFrame.LookVector, false, v_u_32)
            if v_u_32 == 3 then
                v_u_38 = v_u_38 - 1
            elseif v_u_32 == 4 then
                v_u_39 = v_u_39 - 1
            end
            task.wait(0.2)
            unset()
            if v_u_33 == 1 then
                v_u_32 = 1
                setup(v_u_34)
            elseif v_u_33 == 2 then
                v_u_32 = 2
                setup(v_u_35)
            else
                v_u_32 = 1
                v_u_33 = 1
                setup(v_u_34)
            end
            UpdateGui()
            v_u_95 = false
        end
    end
    function Reload()
        -- upvalues: (ref) v_u_48, (ref) v_u_78, (ref) v_u_79, (ref) v_u_77, (ref) v_u_82, (ref) v_u_101
        if v_u_48 and (v_u_48.Type == "Gun" and (v_u_48.StoredAmmo > 0 and (v_u_48.AmmoInGun < v_u_48.Ammo or v_u_48.IncludeChamberedBullet and v_u_48.AmmoInGun < v_u_48.Ammo + 1))) then
            v_u_78 = false
            v_u_79 = false
            v_u_77 = true
            UpdateGui()
            if v_u_48.ShellInsert then
                if v_u_48.AmmoInGun > 0 then
                    for _ = 1, v_u_48.Ammo - v_u_48.AmmoInGun do
                        if v_u_48.StoredAmmo > 0 and v_u_48.AmmoInGun < v_u_48.Ammo then
                            if v_u_82 then
                                break
                            end
                            if v_u_101.Reload then
                                v_u_101.Reload:Play(0.15)
                            end
                            ReloadAnim()
                            v_u_48.AmmoInGun = v_u_48.AmmoInGun + 1
                            local v518 = v_u_48
                            local v519 = v_u_48.StoredAmmo - 1
                            v518.StoredAmmo = math.max(v519, 0)
                            UpdateGui()
                        end
                    end
                else
                    if v_u_101.Reload then
                        v_u_101.Reload:Play(0.15)
                    end
                    TacticalReloadAnim()
                    v_u_48.AmmoInGun = v_u_48.AmmoInGun + 1
                    local v520 = v_u_48
                    local v521 = v_u_48.StoredAmmo - 1
                    v520.StoredAmmo = math.max(v521, 0)
                    UpdateGui()
                    for _ = 1, v_u_48.Ammo - v_u_48.AmmoInGun do
                        if v_u_48.StoredAmmo > 0 and v_u_48.AmmoInGun < v_u_48.Ammo then
                            if v_u_82 then
                                break
                            end
                            if v_u_101.Reload then
                                v_u_101.Reload:Play(0.15)
                            end
                            ReloadAnim()
                            v_u_48.AmmoInGun = v_u_48.AmmoInGun + 1
                            local v522 = v_u_48
                            local v523 = v_u_48.StoredAmmo - 1
                            v522.StoredAmmo = math.max(v523, 0)
                            UpdateGui()
                        end
                    end
                end
            else
                if v_u_101.Reload then
                    v_u_101.Reload:Play(0.15)
                end
                if v_u_48.AmmoInGun > 0 then
                    ReloadAnim()
                    if v_u_48.IncludeChamberedBullet then
                        local v524 = v_u_48.Ammo - v_u_48.AmmoInGun + 1
                        local v525 = v_u_48.StoredAmmo
                        local v526 = math.min(v524, v525)
                        v_u_48.AmmoInGun = v_u_48.AmmoInGun + v526
                        local v527 = v_u_48
                        local v528 = v_u_48.StoredAmmo - v526
                        v527.StoredAmmo = math.max(v528, 0)
                    else
                        local v529 = v_u_48.Ammo - v_u_48.AmmoInGun
                        local v530 = v_u_48.StoredAmmo
                        local v531 = math.min(v529, v530)
                        v_u_48.AmmoInGun = v_u_48.AmmoInGun + v531
                        local v532 = v_u_48
                        local v533 = v_u_48.StoredAmmo - v531
                        v532.StoredAmmo = math.max(v533, 0)
                    end
                else
                    TacticalReloadAnim()
                    local v534 = v_u_48.Ammo - v_u_48.AmmoInGun
                    local v535 = v_u_48.StoredAmmo
                    local v536 = math.min(v534, v535)
                    v_u_48.AmmoInGun = v_u_48.AmmoInGun + v536
                    local v537 = v_u_48
                    local v538 = v_u_48.StoredAmmo - v536
                    v537.StoredAmmo = math.max(v538, 0)
                end
            end
            v_u_79 = true
            v_u_82 = false
            v_u_77 = false
            RunCheck()
            UpdateGui()
        end
    end
    function GunFx()
        -- upvalues: (ref) v_u_88, (ref) v_u_40, (ref) v_u_89, (ref) v_u_55, (ref) v_u_48, (copy) v_u_104, (ref) v_u_56, (ref) v_u_54, (ref) v_u_57, (copy) v_u_4
        if v_u_88 == true then
            v_u_40.Handle.Muzzle.Supressor:Play()
        else
            v_u_40.Handle.Muzzle.Fire:Play()
        end
        if v_u_89 == true then
            v_u_40.Handle.Muzzle.Smoke:Emit(10)
        else
            v_u_40.Handle.Muzzle["FlashFX[Flash]"]:Emit(10)
            v_u_40.Handle.Muzzle.Smoke:Emit(10)
        end
        if v_u_55 then
            local v539 = v_u_48.MaxSpread * v_u_104.MaxSpread
            local v540 = v_u_55 + v_u_48.AimInaccuracyStepAmount * v_u_104.AimInaccuracyStepAmount
            v_u_55 = math.min(v539, v540)
            local v541 = v_u_48.MaxRecoilPower * v_u_104.MaxRecoilPower
            local v542 = v_u_56 + v_u_48.RecoilPowerStepAmount * v_u_104.RecoilPowerStepAmount
            v_u_56 = math.min(v541, v542)
        end
        v_u_54 = v_u_54 + 1
        v_u_57 = os.clock()
        if v_u_48.AmmoInGun > 0 or not v_u_48.SlideLock then
            for _, v543 in pairs(v_u_40.Handle:GetChildren()) do
                if v543:IsA("Motor6D") and string.match(v543.Name, "Slide") then
                    v_u_4:Create(v543, TweenInfo.new(30 / v_u_48.ShootRate, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut, 0, true, 0), {
                        ["C0"] = v_u_48.SlideEx:inverse()
                    }):Play()
                end
            end
        elseif v_u_48.AmmoInGun <= 0 and v_u_48.SlideLock then
            for _, v544 in pairs(v_u_40.Handle:GetChildren()) do
                if v544:IsA("Motor6D") and string.match(v544.Name, "Slide") then
                    v_u_4:Create(v544, TweenInfo.new(30 / v_u_48.ShootRate, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut, 0, false, 0), {
                        ["C0"] = v_u_48.SlideEx:inverse()
                    }):Play()
                end
            end
        end
        v_u_40.Handle.Chamber.Smoke:Emit(10)
        v_u_40.Handle.Chamber.Shell:Emit(1)
    end
    function Shoot()
        -- upvalues: (ref) v_u_48, (ref) v_u_76, (ref) v_u_77, (ref) v_u_74, (ref) v_u_78, (ref) v_u_40, (copy) v_u_126, (copy) v_u_11, (ref) v_u_88, (ref) v_u_89, (copy) v_u_28
        if v_u_48 and (v_u_48.Type == "Gun" and not (v_u_76 or v_u_77)) then
            if v_u_77 or v_u_74 then
                v_u_78 = false
                return
            end
            if v_u_48.AmmoInGun <= 0 or v_u_48.Jammed then
                v_u_40.Handle.Click:Play()
                local v545 = v_u_126
                local v546 = math.random(-1, 1) / 5
                v545:shove((Vector3.new(v546, 0.25, 0)))
                v_u_78 = false
                return
            end
            v_u_78 = true
            delay(0, function()
                -- upvalues: (ref) v_u_48, (ref) v_u_76, (ref) v_u_11, (ref) v_u_40, (ref) v_u_88, (ref) v_u_89, (ref) v_u_28, (ref) v_u_78
                if v_u_48 and v_u_48.ShootType == 1 then
                    v_u_76 = true
                    v_u_11.Atirar:FireServer(v_u_40.Name, v_u_88, v_u_89)
                    for _ = 1, v_u_48.Bullets do
                        v_u_28:Spawn(new_bullet)
                    end
                    local v547 = v_u_48
                    local v548 = v_u_48.AmmoInGun - 1
                    v547.AmmoInGun = math.max(v548, 0)
                    GunFx()
                    UpdateGui()
                    v_u_28:Spawn(Recoil)
                    task.wait(0.016666666666666666)
                    v_u_76 = false
                    return
                end
                if v_u_48 and v_u_48.ShootType == 2 then
                    for _ = 1, v_u_48.BurstShot do
                        if v_u_76 or (v_u_48.AmmoInGun <= 0 or (v_u_78 == false or v_u_48.Jammed)) then
                            ::l11::
                            return
                        end
                        v_u_76 = true
                        v_u_11.Atirar:FireServer(v_u_40.Name, v_u_88, v_u_89)
                        for _ = 1, v_u_48.Bullets do
                            v_u_28:Spawn(new_bullet)
                        end
                        local v549 = v_u_48
                        local v550 = v_u_48.AmmoInGun - 1
                        v549.AmmoInGun = math.max(v550, 0)
                        GunFx()
                        UpdateGui()
                        v_u_28:Spawn(Recoil)
                        task.wait(60 / v_u_48.ShootRate)
                        v_u_76 = false
                    end
                    return
                else
                    if v_u_48 and v_u_48.ShootType == 3 then
                        while v_u_78 and (not v_u_76 and (v_u_48.AmmoInGun > 0 and not v_u_48.Jammed)) do
                            v_u_76 = true
                            v_u_11.Atirar:FireServer(v_u_40.Name, v_u_88, v_u_89)
                            for _ = 1, v_u_48.Bullets do
                                v_u_28:Spawn(new_bullet)
                            end
                            local v551 = v_u_48
                            local v552 = v_u_48.AmmoInGun - 1
                            v551.AmmoInGun = math.max(v552, 0)
                            GunFx()
                            UpdateGui()
                            v_u_28:Spawn(Recoil)
                            task.wait(60 / v_u_48.ShootRate)
                            v_u_76 = false
                        end
                    elseif v_u_48 and v_u_48.ShootType == 4 or v_u_48 and v_u_48.ShootType == 5 then
                        v_u_76 = true
                        v_u_11.Atirar:FireServer(v_u_40.Name, v_u_88, v_u_89)
                        for _ = 1, v_u_48.Bullets do
                            v_u_28:Spawn(new_bullet)
                        end
                        local v553 = v_u_48
                        local v554 = v_u_48.AmmoInGun - 1
                        v553.AmmoInGun = math.max(v554, 0)
                        GunFx()
                        UpdateGui()
                        v_u_28:Spawn(Recoil)
                        PumpAnim()
                        RunCheck()
                        v_u_76 = false
                    end
                    goto l11
                end
            end)
        end
    end
    v_u_139.JumpPower = 30
    v_u_139.Running:Connect(function(p555)
        -- upvalues: (ref) v_u_72, (ref) v_u_73
        v_u_72 = p555
        if p555 > 0.1 then
            v_u_73 = true
        else
            v_u_73 = false
        end
    end)
    v_u_139.Jumping:Connect(function(_)
        -- upvalues: (copy) v_u_126
        v_u_126:shove(Vector3.new(0, -0.5, 0))
    end)
    v_u_139.Changed:connect(function(p556)
        -- upvalues: (copy) v_u_139, (ref) v_u_83, (ref) v_u_75, (copy) v_u_223
        if p556 == "Jump" and v_u_139.Sit == false then
            if v_u_83 then
                v_u_139.Jump = false
                return
            end
            v_u_83 = true
            if v_u_75 then
                v_u_75 = false
                v_u_223(v_u_75)
            end
            delay(0, function()
                -- upvalues: (ref) v_u_83
                wait(1.5)
                v_u_83 = false
            end)
        end
    end)
    v_u_139.Died:Connect(function(_)
        -- upvalues: (copy) v_u_3, (copy) v_u_4, (copy) v_u_23, (ref) v_u_138, (ref) v_u_129, (ref) v_u_130, (ref) v_u_131, (ref) v_u_132, (ref) v_u_79, (ref) v_u_32, (copy) v_u_2, (copy) v_u_8, (copy) v_u_22
        v_u_3:UnbindFromRenderStep("Render_Viewmodel")
        v_u_4:Create(v_u_23.Humanoid, TweenInfo.new(1), {
            ["CameraOffset"] = Vector3.new(0, 0, 0)
        }):Play()
        v_u_138 = false
        Stand()
        v_u_129 = 0
        v_u_130 = 0
        v_u_131 = 0
        v_u_132 = 0
        Lean()
        v_u_79 = true
        v_u_32 = 0
        unset()
        v_u_2:UnbindAction("Fire")
        v_u_2:UnbindAction("ADS")
        v_u_2:UnbindAction("Reload")
        v_u_2:UnbindAction("Melee")
        v_u_2:UnbindAction("EquipPrimary")
        v_u_2:UnbindAction("EquipSecondary")
        v_u_2:UnbindAction("EquipCamera")
        v_u_2:UnbindAction("PlaceDrone")
        v_u_2:UnbindAction("Run")
        v_u_2:UnbindAction("Prone")
        v_u_2:UnbindAction("Crouch")
        v_u_2:UnbindAction("Grenade")
        v_u_2:UnbindAction("ToggleWalk")
        v_u_2:UnbindAction("LeanLeft")
        v_u_2:UnbindAction("LeanRight")
        v_u_8:RemoveTag(v_u_22, "ADS")
    end)
    v_u_139.StateChanged:connect(function(_, p557)
        -- upvalues: (ref) v_u_134, (copy) v_u_142, (copy) v_u_28, (copy) v_u_58, (copy) v_u_22, (copy) v_u_125, (copy) v_u_126, (copy) v_u_18, (copy) v_u_139, (copy) v_u_5, (copy) v_u_11
        if p557 == Enum.HumanoidStateType.Freefall and not v_u_134 then
            v_u_134 = true
            local v558 = 0
            local v559 = 0
            while v_u_134 do
                v559 = v_u_142.Velocity.magnitude
                v558 = v558 + 1
                v_u_28:Wait()
            end
            local v560 = (v559 - 75) * 1
            if v560 > 5 and v558 > 20 then
                local v561 = v_u_58 .. "-" .. v_u_22.UserId
                local v562 = v_u_125
                local v563 = -v560 / 20
                local v564 = math.random(-v560, v560) / 5
                v562:shove((Vector3.new(v563, 0, v564)))
                local v565 = v_u_126
                local v566 = math.random(-v560, v560) / 5
                local v567 = v560 / 5
                v565:shove((Vector3.new(v566, v567, 0)))
                local v568 = v_u_18.FallDamage:Clone()
                v568.Parent = v_u_22.PlayerGui
                v568.Volume = v560 / v_u_139.MaxHealth
                v568:Play()
                v_u_5:AddItem(v568, v568.TimeLength)
                v_u_11.Damage:FireServer(nil, nil, nil, nil, nil, true, v560, v561)
                return
            end
        elseif p557 == Enum.HumanoidStateType.Landed or p557 == Enum.HumanoidStateType.Dead then
            v_u_134 = false
            v_u_126:shove(Vector3.new(0, 0.5, 0))
        end
    end)
    function RunCheck()
        -- upvalues: (ref) v_u_74, (ref) v_u_78, (ref) v_u_101, (ref) v_u_75
        if v_u_74 then
            v_u_78 = false
            if v_u_101.Sprint then
                v_u_101.Sprint:Play(0.15)
            end
            for _, v569 in pairs(v_u_101) do
                if v569 ~= v_u_101.Sprint and v569 ~= v_u_101.Reload then
                    v569:Stop(0.15)
                end
            end
            SprintAnim()
        else
            if v_u_75 then
                if v_u_101.Aim then
                    v_u_101.Aim:Play(0.15)
                end
                for _, v570 in pairs(v_u_101) do
                    if v570 ~= v_u_101.Aim and v570 ~= v_u_101.Reload then
                        v570:Stop(0.15)
                    end
                end
            else
                if v_u_101.Idle then
                    v_u_101.Idle:Play(0.15)
                end
                for _, v571 in pairs(v_u_101) do
                    if v571 ~= v_u_101.Idle and v571 ~= v_u_101.Reload then
                        v571:Stop(0.15)
                    end
                end
            end
            IdleAnim()
        end
        SpeedCheck()
    end
    function Stand()
        -- upvalues: (copy) v_u_128, (ref) v_u_129, (ref) v_u_130, (copy) v_u_4, (copy) v_u_23, (ref) v_u_131, (ref) v_u_132
        if Crouch or Prone then
            v_u_128:FireServer(v_u_129, v_u_130)
            local v572 = v_u_4
            local v573 = v_u_23.Humanoid
            local v574 = TweenInfo.new(0.3)
            local v575 = {}
            local v576 = v_u_131
            local v577 = v_u_132
            v575.CameraOffset = Vector3.new(v576, v577, 0)
            v572:Create(v573, v574, v575):Play()
        end
    end
    function Crouch()
        -- upvalues: (copy) v_u_128, (ref) v_u_129, (ref) v_u_130, (copy) v_u_4, (copy) v_u_23, (ref) v_u_131, (ref) v_u_132
        v_u_128:FireServer(v_u_129, v_u_130)
        local v578 = v_u_4
        local v579 = v_u_23.Humanoid
        local v580 = TweenInfo.new(0.3)
        local v581 = {}
        local v582 = v_u_131
        local v583 = v_u_132
        v581.CameraOffset = Vector3.new(v582, v583, 0)
        v578:Create(v579, v580, v581):Play()
    end
    function Prone()
        -- upvalues: (copy) v_u_128, (ref) v_u_129, (ref) v_u_130, (copy) v_u_4, (copy) v_u_23, (ref) v_u_131, (ref) v_u_132
        v_u_128:FireServer(v_u_129, v_u_130)
        local v584 = v_u_4
        local v585 = v_u_23.Humanoid
        local v586 = TweenInfo.new(0.3)
        local v587 = {}
        local v588 = v_u_131
        local v589 = v_u_132
        v587.CameraOffset = Vector3.new(v588, v589, 0)
        v584:Create(v585, v586, v587):Play()
    end
    function Lean()
        -- upvalues: (copy) v_u_4, (copy) v_u_23, (ref) v_u_131, (ref) v_u_132, (copy) v_u_128, (ref) v_u_129, (ref) v_u_130, (ref) v_u_133, (copy) v_u_18, (copy) v_u_142, (copy) v_u_5
        local v590 = v_u_4
        local v591 = v_u_23.Humanoid
        local v592 = TweenInfo.new(0.4)
        local v593 = {}
        local v594 = v_u_131
        local v595 = v_u_132
        v593.CameraOffset = Vector3.new(v594, v595, 0)
        v590:Create(v591, v592, v593):Play()
        v_u_128:FireServer(v_u_129, v_u_130)
        if v_u_133 ~= v_u_131 then
            v_u_133 = v_u_131
            local v596 = v_u_18.Move:GetChildren()
            local v597 = v596[math.random(#v596)]:Clone()
            local v598 = v_u_23.ClientConfig:GetAttribute("Loudness")
            v597.Parent = v_u_142
            v597.PlaybackSpeed = math.random(30, 55) / 40
            v597.Volume = 0.5 * v598
            v597.RollOffMinDistance = 5 * v598
            v597.RollOffMaxDistance = 25 * v598
            v597:Play()
            v_u_5:AddItem(v597, v597.TimeLength)
        end
    end
    function EquipAnim()
        -- upvalues: (ref) v_u_81, (ref) v_u_79, (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
        v_u_81 = false
        v_u_79 = false
        pcall(function()
            -- upvalues: (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
            if v_u_49 then
                local v599 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_49.EquipAnim(v599)
            else
                local v600 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_48.EquipAnim(v600)
            end
        end)
        v_u_79 = true
        v_u_81 = true
    end
    function UnEquipAnim()
        -- upvalues: (ref) v_u_81, (ref) v_u_79, (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
        v_u_81 = false
        v_u_79 = false
        pcall(function()
            -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
            local v601 = {
                v_u_46,
                v_u_45,
                v_u_47,
                v_u_40,
                v_u_41
            }
            v_u_48.UnEquipAnim(v601)
        end)
        v_u_79 = true
    end
    function IdleAnim()
        -- upvalues: (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48, (ref) v_u_81
        pcall(function()
            -- upvalues: (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
            if v_u_49 then
                local v602 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_49.IdleAnim(v602)
            else
                local v603 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_48.IdleAnim(v603)
            end
        end)
        v_u_81 = true
    end
    function SprintAnim()
        -- upvalues: (ref) v_u_81, (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
        v_u_81 = false
        pcall(function()
            -- upvalues: (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
            if v_u_49 then
                local v604 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_49.SprintAnim(v604)
            else
                local v605 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_48.SprintAnim(v605)
            end
        end)
    end
    function ReloadAnim()
        -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
        pcall(function()
            -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
            local v606 = {
                v_u_46,
                v_u_45,
                v_u_47,
                v_u_40,
                v_u_41
            }
            v_u_48.ReloadAnim(v606)
        end)
    end
    function TacticalReloadAnim()
        -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
        pcall(function()
            -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
            local v607 = {
                v_u_46,
                v_u_45,
                v_u_47,
                v_u_40,
                v_u_41
            }
            v_u_48.TacticalReloadAnim(v607)
        end)
    end
    function PumpAnim()
        -- upvalues: (ref) v_u_77, (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
        v_u_77 = true
        pcall(function()
            -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
            local v608 = {
                v_u_46,
                v_u_45,
                v_u_47,
                v_u_40,
                v_u_41
            }
            v_u_48.PumpAnim(v608)
        end)
        v_u_77 = false
    end
    function meleeAttack()
        -- upvalues: (ref) v_u_79, (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
        v_u_79 = false
        pcall(function()
            -- upvalues: (ref) v_u_49, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41, (ref) v_u_48
            if v_u_49 then
                local v609 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_49.meleeAttack(v609)
            else
                local v610 = {
                    v_u_46,
                    v_u_45,
                    v_u_47,
                    v_u_40,
                    v_u_41
                }
                v_u_48.meleeAttack(v610)
            end
        end)
        v_u_79 = true
    end
    function GrenadeThrow()
        -- upvalues: (ref) v_u_79, (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
        v_u_79 = false
        pcall(function()
            -- upvalues: (ref) v_u_48, (ref) v_u_46, (ref) v_u_45, (ref) v_u_47, (ref) v_u_40, (ref) v_u_41
            local v611 = {
                v_u_46,
                v_u_45,
                v_u_47,
                v_u_40,
                v_u_41
            }
            v_u_48.GrenadeThrow(v611)
        end)
        v_u_79 = true
    end
    v_u_2:BindAction("EquipPrimary", v330, true, Enum.KeyCode.One)
    v_u_2:BindAction("EquipSecondary", v330, true, Enum.KeyCode.Two)
    v_u_2:BindAction("EquipUtility", v330, true, Enum.KeyCode.G, Enum.KeyCode.Three)
    v_u_2:BindAction("EquipGadget", v330, true, Enum.KeyCode.Four)
    v_u_2:BindAction("EquipCamera", v330, true, Enum.KeyCode.Five)
    v_u_2:BindAction("PlaceDrone", function(p612, p613, _)
        -- upvalues: (copy) v_u_22, (copy) v_u_11
        if p612 == "PlaceDrone" and p613 == Enum.UserInputState.Begin then
            if not v_u_22.Character or not v_u_22.Character:FindFirstChild("Humanoid") and v_u_22.Character.Health <= 0 then
                return
            end
            if v_u_22.TeamColor == game.Teams.Attackers.TeamColor then
                v_u_11.PlaceDrone:FireServer()
            end
        end
    end, true, Enum.KeyCode.Six)
    v_u_2:BindAction("Run", v339, true, Enum.KeyCode.LeftShift)
    v_u_2:BindAction("Prone", v339, true, Enum.KeyCode.LeftControl)
    v_u_2:BindAction("Crouch", v339, true, Enum.KeyCode.C)
    v_u_2:BindAction("ToggleWalk", v339, true, Enum.KeyCode.LeftAlt)
    v_u_2:BindAction("LeanLeft", v333, true, Enum.KeyCode.Q)
    v_u_2:BindAction("LeanRight", v333, true, Enum.KeyCode.E)
    local function v624(p614, p615)
        -- upvalues: (copy) v_u_6, (ref) v_u_34, (ref) v_u_35, (ref) v_u_36, (ref) v_u_37, (copy) v_u_20, (ref) v_u_38, (ref) v_u_120, (copy) v_u_19, (ref) v_u_39, (copy) v_u_24, (copy) v_u_22, (ref) v_u_80
        if p614 and (p614 ~= "" and v_u_6.Game.Classes:FindFirstChild(p614)) then
            local v616 = require(v_u_6.Game.Classes[p614][p615.Primary])
            local v617 = require(v_u_6.Game.Classes[p614][p615.Secondary])
            v_u_34 = p615.Primary
            v_u_35 = p615.Secondary
            v_u_36 = p615.Utility
            v_u_37 = p615.Gadget
            if p615.Primary == "" or not v_u_20[p614]:FindFirstChild(p615.Primary) then
                print("Couldn\'t Find Primary Weapon")
            else
                local v618 = v_u_20[p614][p615.Primary]:Clone()
                v618.Parent = script.Parent.GModule
                local v619 = require(v618)
                v619.SightAtt = v616.SightAtt
                v619.BarrelAtt = v616.BarrelAtt
                v619.UnderBarrelAtt = v616.UnderBarrelAtt
                v619.OtherAtt = v616.OtherAtt
                v619.SkinTable = v616.SkinTable
            end
            if p615.Secondary == "" or not v_u_20[p614]:FindFirstChild(p615.Secondary) then
                print("Couldn\'t Find Secondary Weapon")
            else
                local v620 = v_u_20[p614][p615.Secondary]:Clone()
                v620.Parent = script.Parent.GModule
                local v621 = require(v620)
                v621.SightAtt = v617.SightAtt
                v621.BarrelAtt = v617.BarrelAtt
                v621.UnderBarrelAtt = v617.UnderBarrelAtt
                v621.OtherAtt = v617.OtherAtt
                v621.SkinTable = v617.SkinTable
            end
            if p615.Utility == "" or not v_u_20[p614]:FindFirstChild(p615.Utility) then
                print("Couldn\'t Find Grenade")
            else
                local v622 = v_u_20[p614][p615.Utility]:Clone()
                v622.Parent = script.Parent.GModule
                v_u_38 = require(v622).Ammo
                v_u_120.HealthHud.Ut.ImageLabel.Image = v_u_19.GadgetImg:FindFirstChild(v622.Name) and v_u_19.GadgetImg[v622.Name].Texture or "http://www.roblox.com/asset/?id=7104816039"
            end
            if p615.Gadget == "" or not v_u_20[p614]:FindFirstChild(p615.Gadget) then
                print("Couldn\'t Find Gadget")
            else
                local v623 = v_u_20[p614][p615.Gadget]:Clone()
                v623.Parent = script.Parent.GModule
                v_u_39 = require(v623).Ammo
                v_u_120.HealthHud.Gr.ImageLabel.Image = v_u_19.GadgetImg:FindFirstChild(v623.Name) and v_u_19.GadgetImg[v623.Name].Texture or "http://www.roblox.com/asset/?id=7104816039"
            end
            v_u_24.CameraSubject = v_u_22.Character
            v_u_22.CameraMode = Enum.CameraMode.LockFirstPerson
            v_u_80 = false
            setup(v_u_34)
            v_u_80 = true
        else
            warn("Class Does Not Exist")
        end
    end
    Stand()
    v_u_32 = 1
    local v625 = v_u_22:WaitForChild("playerStats")
    if not v625 then
        return
    end
    local v626 = v625:WaitForChild("Operator")
    if not v626 then
        return
    end
    local v627 = v_u_19.Classes:FindFirstChild(v626.Value)
    if not v627 then
        return
    end
    local v628 = require(v627)
    v624(v21.GetClass:InvokeServer(v628))
end
local v_u_629 = v_u_23.Humanoid.MaxHealth
v121:Play()
v122:Play()
v_u_120.HealthHud.Health.HealthText.Text = v_u_23.Humanoid.MaxHealth
v_u_23.Humanoid.HealthChanged:Connect(function(p630)
    -- upvalues: (ref) v_u_120, (copy) v_u_4, (copy) v_u_139, (ref) v_u_629
    local v631 = v_u_120.HealthHud.Health.HealthText
    local v632 = math.ceil(p630)
    v631.Text = math.max(0, v632)
    v_u_4:Create(v_u_120.HealthHud.Health.RedBar, TweenInfo.new(3, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {
        ["Size"] = UDim2.new(p630 / v_u_139.MaxHealth, 0, 1, 0)
    }):Play()
    v_u_120.HealthHud.Health.Bar.Size = UDim2.new(p630 / v_u_139.MaxHealth, 0, 1, 0)
    v_u_120.Efeitos.Health.ImageTransparency = (p630 - v_u_139.MaxHealth / 2) / (v_u_139.MaxHealth / 2)
    v_u_120.Efeitos.LowHealth.ImageTransparency = p630 / (v_u_139.MaxHealth / 2)
    if p630 < v_u_629 then
        v_u_120.HealthHud.Health.Bar.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
        local v633 = 1 - p630 / v_u_629
        game.Lighting.HurtBlur.Size = v633 * 25
        v_u_4:Create(game.Lighting.HurtBlur, TweenInfo.new(3 * v633, Enum.EasingStyle.Sine, Enum.EasingDirection.In, 0, false, 0), {
            ["Size"] = 0
        }):Play()
        if p630 < v_u_139.MaxHealth / 2 then
            game.SoundService.GameSounds.Fx.NearDeathEffect.HighGain = -100 * v633
            game.SoundService.GameSounds.Fx.NearDeathEffect.MidGain = -100 * v633
            game.SoundService.GameSounds.Fx.NearDeathEffect.LowGain = -100 * v633
            v_u_4:Create(game.SoundService.GameSounds.Fx.NearDeathEffect, TweenInfo.new(3 * v633, Enum.EasingStyle.Sine, Enum.EasingDirection.In, 0, false), {
                ["HighGain"] = 0,
                ["MidGain"] = 0,
                ["LowGain"] = 0
            }):Play()
        end
    elseif v_u_629 < p630 then
        v_u_120.HealthHud.Health.Bar.BackgroundColor3 = Color3.fromRGB(0, 100, 170)
    end
    v_u_4:Create(v_u_120.HealthHud.Health.Bar, TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
        ["BackgroundColor3"] = Color3.fromRGB(85, 170, 127)
    }):Play()
    v_u_629 = p630
end)
v_u_1.InputBegan:Connect(function(p634, p635)
    -- upvalues: (ref) v_u_98
    if not p635 then
        if p634.KeyCode == Enum.KeyCode.A then
            v_u_98 = Vector2.new(-1, v_u_98.Y)
        end
        if p634.KeyCode == Enum.KeyCode.D then
            v_u_98 = Vector2.new(v_u_98.X, 1)
        end
    end
end)
v_u_1.InputEnded:Connect(function(p636, p637)
    -- upvalues: (ref) v_u_98
    if not p637 then
        if p636.KeyCode == Enum.KeyCode.A then
            v_u_98 = Vector2.new(0, v_u_98.Y)
        end
        if p636.KeyCode == Enum.KeyCode.D then
            v_u_98 = Vector2.new(v_u_98.X, 0)
        end
    end
end)
v_u_8:GetInstanceAddedSignal("Slow"):Connect(function()
    SpeedCheck()
end)
v_u_8:GetInstanceAddedSignal("Interacting"):Connect(function()
    SpeedCheck()
    unset()
    setup("Interact")
end)
v_u_8:GetInstanceRemovedSignal("Slow"):Connect(function()
    SpeedCheck()
end)
v_u_8:GetInstanceRemovedSignal("Interacting"):Connect(function()
    -- upvalues: (ref) v_u_33, (ref) v_u_32, (ref) v_u_34, (ref) v_u_35
    SpeedCheck()
    unset()
    if v_u_33 == 1 then
        v_u_32 = 1
        setup(v_u_34)
        return
    elseif v_u_33 == 2 then
        v_u_32 = 2
        setup(v_u_35)
    else
        v_u_32 = 1
        v_u_33 = 1
        setup(v_u_34)
    end
end)
