local StarterGui = game:GetService("StarterGui")

local flagtables = {
    -- Performance & Task Scheduler
    ["DFIntTaskSchedulerTargetFps"] = "9999",
    ["FIntTaskSchedulerAutoThreadLimit"] = "6",
    ["FIntTaskSchedulerAsyncTasksMinimumThreadCount"] = "2",
    ["FIntTaskSchedulerMaxNumOfJobs"] = "86",
    ["FIntTaskSchedulerThreadMin"] = "1",

    -- DFFlags
    ["DFFlagBrowserTrackerIdTelemetryEnabled"] = "False",
    ["DFFlagPreloadAsyncSupportTexturePack"] = "True",
    ["DFFlagTextureQualityOverrideEnabled"] = "True",
    ["DFFlagVideoCaptureServiceEnabled"] = "False",
    ["DFFlagSampleAndRefreshRakPing"] = "True",
    ["DFFlagRakNetUseSlidingWindow4"] = "True",
    ["DFFlagCoreScriptTelemetry2"] = "False",
    ["DFFlagEnableSoundPreloading"] = "True",
    ["DFFlagOptimizePartsInPart"] = "True",
    ["DFFlagDisableDPIScale"] = "True",
    ["DFFlagDebugPerfMode"] = "True",

    -- Network / RakNet
    ["DFIntRaknetBandwidthInfluxHundredthsPercentageV2"] = "10000",
    ["DFIntRakNetClockDriftAdjustmentPerPingMillisecond"] = "100",
    ["DFIntRaknetBandwidthPingSendEveryXSeconds"] = "1",
    ["DFIntRakNetNakResendDelayRttPercent"] = "50",
    ["DFIntRakNetNakResendDelayMsMax"] = "100",
    ["DFIntRakNetNakResendDelayMs"] = "10",
    ["DFIntRakNetResendRttMultiple"] = "1",
    ["DFIntRakNetSelectTimeoutMs"] = "1",
    ["DFIntRakNetLoopMs"] = "1",
    ["DFIntRakNetMinAckGrowthPercent"] = "0",
    ["DFIntRakNetMtuValue1InBytes"] = "1280",
    ["DFIntRakNetMtuValue2InBytes"] = "1240",
    ["DFIntRakNetMtuValue3InBytes"] = "1200",
    ["DFIntConnectionMTUSize"] = "1260",

    -- Client Packet / Networking
    ["DFIntMaxReceiveToDeserializeLatencyMilliseconds"] = "15",
    ["DFIntNetworkInDeserializeLimitGameplayMsClient"] = "6",
    ["DFIntNetworkInProcessLimitGameplayMsClient"] = "6",
    ["DFIntClientPacketHealthyAllocationPercent"] = "20",
    ["DFIntClientPacketMaxFrameMicroseconds"] = "200",
    ["DFIntClientPacketExcessMicroseconds"] = "1000",
    ["DFIntClientPacketMinMicroseconds"] = "1",
    ["DFIntClientPacketMaxDelayMs"] = "11",
    ["DFIntMaxWaitTimeBeforeForcePacketProcessMS"] = "1",
    ["DFIntMaxProcessPacketsStepsPerCyclic"] = "5000",
    ["DFIntMaxProcessPacketsStepsAccumulated"] = "0",
    ["DFIntMaxProcessPacketsJobScaling"] = "10000",
    ["DFIntLargePacketQueueSizeCutoffMB"] = "1000",
    ["DFIntDataSenderRate"] = "1000",
    ["DFIntDataSenderMaxBandwidthBps"] = "2147483647",
    ["DFIntDataSenderMaxJoinBandwidthBps"] = "2147483647",
    ["DFIntS2PhysicsSenderRate"] = "1000",
    ["DFIntS2NumPhysicsPacketsPerStep"] = "100",
    ["DFIntPhysicsSenderMaxBandwidthBps"] = "2147483647",
    ["DFIntPhysicsSenderMaxBandwidthBpsScaling"] = "1000",
    ["FIntPGSAngularDampingPermilPersecond"] = "0",
    ["DFFlagPhysicsSkipNonRealTimeHumanoidForceCalc2"] = "True",
    ["FFlagDebugDisplayFPS"] = "True",

    -- SignalR
    ["DFIntSignalRHubConnectionHeartbeatTimerRateMs"] = "1000",
    ["DFIntSignalRHubConnectionBaseRetryTimeMs"] = "100",
    ["DFIntSignalRCoreKeepAlivePingPeriodMs"] = "250",
    ["DFIntSignalRCoreServerTimeoutMs"] = "11100",
    ["DFIntSignalRCoreTimerMs"] = "750",
    ["DFIntSignalRCoreRpcQueueSize"] = "256",

    -- Animation / Rendering
    ["DFIntAnimationLodFacsVisibilityDenominator"] = "0",
    ["DFIntAnimationLodFacsDistanceMin"] = "0",
    ["DFIntAnimationLodFacsDistanceMax"] = "0",
    ["DFIntDebugFRMQualityLevelOverride"] = "1",
    ["DFIntDebugDynamicRenderKiloPixels"] = "1100",
    ["DFIntDebugRestrictGCDistance"] = "1",

    -- Texture quality (low / blurry textures)
    ["DFFlagTextureQualityOverrideEnabled"] = "True",
    ["DFIntTextureQualityOverride"] = "0",

    -- Wait Timers
    ["DFIntWaitOnUpdateNetworkLoopEndedMS"] = "100",
    ["DFIntWaitOnRecvFromLoopEndedMS"] = "100",

    -- FInt Rendering / Graphics
    ["FIntRenderMaxShadowAtlasUsageBeforeDownscale"] = "80",
    ["FIntRenderShadowMapDepthCacheMemLimit"] = "192",
    ["FIntUITextureMaxRenderTextureSize"] = "1024",
    ["FIntRakNetResendBufferArrayLength"] = "128",
    ["FIntTerrainOTAMaxTextureSize"] = "1024",
    ["FIntOcclusionWorkerThreadCount"] = "5",
    ["FIntDefaultMeshCacheSizeMB"] = "256",
    ["FIntRobloxGuiBlurIntensity"] = "0",
    ["FIntTerrainArraySliceSize"] = "0",
    ["FIntDebugForceMSAASamples"] = "1",
    ["FIntRenderShadowmapBias"] = "0",
    ["FIntFRMMaxGrassDistance"] = "0",
    ["FIntFRMMinGrassDistance"] = "0",
    ["FIntGrassMovementReducedMotionFactor"] = "0",
    ["FIntDebugTextureManagerSkipMips"] = "7",
    ["FIntPerformanceTelemetryQueueProcessLimit"] = "0",
    ["FIntTelemetryProfilerFrequency"] = "0",
    ["FIntRenderLocalLightFadeInMs"] = "0",
    ["FIntReportDeviceInfoRollout"] = "0",

    -- FFlags
    ["FFlagRenderAllocateShadowMapResourcesOnDemand"] = "True",
    ["FFlagSpecifyNetworkReplicatorScopeForItems"] = "True",
    ["FFlagTaskSchedulerLimitTargetFpsTo2402"] = "False",
    ["FFlagHandleAltEnterFullscreenManually"] = "False",
    ["FFlagGameBasicSettingsFramerateCap5"] = "False",
    ["FFlagSpecifyNetworkReplicatorScope"] = "True",
    ["FFlagSendRenderFidelityTelemetry2"] = "False",
    ["FFlagRenderGpuTextureCompressor"] = "True",
    ["FFlagBaseThreadPoolUseRuntime2"] = "True",
    ["FFlagCacheTextBoundsInGuiText"] = "True",
    ["FFlagEnableTelemetryService1"] = "False",
    ["FFlagDebugGraphicsPreferD3D11"] = "True",
    ["FFlagPerfDataOnTelemetryV2"] = "False",
    ["FFlagOpenTelemetryEnabled2"] = "False",
    ["FFlagRbxStorageUseMemCache"] = "True",
    ["FFlagDebugForceGenerateHSR"] = "True",
    ["FFlagRenderInitShadowmaps"] = "True",
    ["FFlagFastGPULightCulling3"] = "True",
    ["FFlagDebugSkyGray"] = "True",
    ["FFlagDebugRenderingSetDeterministic"] = "True",
    ["FLogNetwork"] = "7"
}

-- Executors expect the flag name WITHOUT its type prefix (e.g. "TaskSchedulerTargetFps")
local function formatFlag(z)
    z = z:gsub("^DFInt", "")
    z = z:gsub("^DFFlag", "")
    z = z:gsub("^FFlag", "")
    z = z:gsub("^FInt", "")
    z = z:gsub("FString", "")
    z = z:gsub("FLog", "")
    return z
end

if not setfflag then
    return
end

for k, v in pairs(flagtables) do
    pcall(function()
        local formatted = formatFlag(k)
        if getfflag and getfflag(formatted) then
            setfflag(formatted, v)
        elseif getfflag and getfflag(k) then
            setfflag(k, v)
        else
            setfflag(formatted, v)
        end
    end)
end

pcall(function()
    StarterGui:SetCore("SendNotification", {
        Title = "Flags Applied",
        Text = "Rejoin for flags to apply.",
        Duration = 5
    })
end)
