local mamali = 179286096
local soheil = 166709132

local function run(msg, matches)

  local hash = 'rank:'..msg.to.id..':variables'
  local text = ''
    local value = redis:hget(hash, msg.from.id)
     if not value then
        if msg.from.id == tonumber(Arian) then
           text = text..'???? ???? ?? ???? \n\n'
         elseif msg.from.id == tonumber(Sosha) then
         text = text..'???? ???? ???? ???? (Full Access Admin) \n\n'
         elseif is_admin2(msg.from.id) then
           text = text..'???? ????? \n\n'
         elseif is_owner2(msg.from.id, msg.to.id) then
           text = text..'???? ???? ?? ???? \n\n'
         elseif is_momod2(msg.from.id, msg.to.id) then
           text = text..'???? ???? ???? \n\n'
     else
           text = text..'????\n\n'
      end
      else
       text = text..'???? '..value..'  \n\n'
     end
   reply_msg(msg.id, text, ok_cb,  true)
    
end

return {
  patterns = {


"^[Ss]lm$",
"^[Ss]alam$",
"^????$",
"^[Hh]ello$",
"^[Hh]elo$",
"^[Hh]i$",
"^?????$",

  }, 
  run = run 
}
