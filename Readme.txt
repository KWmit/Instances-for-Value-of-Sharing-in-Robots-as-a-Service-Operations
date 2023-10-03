1. Each instance is named in the format "Instance-Machines-WR-Fields-Index"
2. Each instance file is saved in JLD2 format in Julia. The structure of each instance file is as follows:
    n::Int (number of fields)
    K::Int (number of machines)
    D::Int (number of days)
    maxHours::Int (maximum working hours)
    workNeeded::Vector{Float64} (a vector of working hours needed for each field)
    clientDays::Array{Int,2} (a matrix showing available days for working for each field)
    timeTravel::Array{Float64,2} (a travel time matrix between nodes)
    wages::Array{Array{Float64,1},1} (coefficients of the piece-wise linear functions for labor cost)
    c_T::Float64 (unit travel cost)
    c_W::Float64 (unit machine cost for working)