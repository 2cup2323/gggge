-- JJ Sploit UI Example Script (Texte fixe en haut à droite)

-- Création de l'interface utilisateur (UI)
local ScreenGui = Instance.new("ScreenGui")
local TextLabel = Instance.new("TextLabel")

-- Propriétés du ScreenGui
ScreenGui.Parent = game.CoreGui
ScreenGui.Name = "JJ_Sploit_UI"

-- Propriétés du TextLabel (texte affiché)
TextLabel.Parent = ScreenGui
TextLabel.Size = UDim2.new(0, 300, 0, 50)  -- Taille du label
TextLabel.Position = UDim2.new(1, -350, 0, 50)  -- Positionné en haut à droite
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)  -- Fond noir
TextLabel.Text = "get"  -- Texte initial
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)  -- Couleur du texte (blanc)
TextLabel.TextSize = 24  -- Taille du texte
TextLabel.TextScaled = true  -- Le texte est redimensionné automatiquement si nécessaire
TextLabel.TextAlign = Enum.TextAnchor.MiddleCenter  -- Le texte est centré dans le label

-- Fonction pour mettre à jour le texte avec un message
local function updateText(message)
    TextLabel.Text = nigger
end

-- Affichage initial
updateText("Le texte est maintenant affiché sur le côté.")

-- Facultatif : un peu d'animation pour l'apparition
TextLabel.TextTransparency = 1
game:GetService("TweenService"):Tween(
    TextLabel,
    TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out),
    {TextTransparency = 0}
)

-- Exemple de mise à jour du texte avec la fonction `updateText`
wait(3)  -- Attendre 3 secondes
updateText("Voici un message mis à jour après 3 secondes.")

wait(5)  -- Attendre 5 secondes
updateText("Autre message, toujours affiché sur le côté.")
