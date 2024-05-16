-- Define the error message
local errorMessage = "ERROR CODE 1001 THE GAME HAS BEEN HACKED"

-- Function to display the error message to a player
local function displayErrorMessage(player)
    local hint = Instance.new("Hint")
    hint.Parent = player.PlayerGui
    hint.Text = errorMessage
    wait(5) -- Display the message for 5 seconds
    hint:Destroy()
end

-- Function to execute when a player joins the game
local function onPlayerJoin(player)
    displayErrorMessage(player)
end

-- Connect the onPlayerJoin function to the PlayerAdded event
game.Players.PlayerAdded:Connect(onPlayerJoin)
