<template>
    <div>
        <UploadLayout>
            <div class="w-full mt-[80px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4">
                <div>
                    <div class="text-[23px] font-semibold">Upload video</div>
                    <div class="text-gray-400 mt-1">Post a video to your account</div>
                </div>

                <div class="mt-8 md:flex gap-6">
                    <label
                        v-if="false"
                        for="fileInput"
                        class="
                            cursor-pointer
                            md:mx-0
                            mx-auto
                            mt-4
                            mb-6
                            flex
                            flex-col
                            items-center
                            justify-center
                            w-full
                            max-w-[260px]
                            h-[470px]
                            text-center
                            p-3
                            border-2
                            border-dashed
                            border-gray-300
                            rounded-lg
                            hover:bg-gray-100
                            cursor:pointer
                        "
                    >
                        <Icon name="majesticons:cloud-upload" size="40" color="#B3B3B1" />
                        <div class="mt-4 text-[17px]">Select video to upload</div>
                        <div class="mt-1.5 text-gray-500 text-[13px]">Or drag and drop a file</div>
                        <div class="mt-12 text-gray-400 text-sm">MP4</div>
                        <div class="mt-2 text-gray-400 text-[13px]">Up to 30 minutes</div>
                        <div class="mt-2 text-gray-400 text-[13px]">Less than 2 GB</div>
                        <div class="px-2 py-1.5 mt-8 text-white text-[15px] w-[80%] bg-[#F02C56] rounded-sm">
                            Select file
                        </div>
                        <input
                            ref="file"
                            type="file"
                            id="fileInput"
                            hidden
                            accept=".mp4"
                        >
                    </label>

                    <div
                        v-else
                        class="
                            md:mx-0
                            mx-auto
                            mt-4
                            md:mb-12
                            mb-16
                            flex
                            items-center
                            justify-center
                            w-full
                            max-w-[260px]
                            h-[540px]
                            p-3
                            rounded-2xl
                            cursor-pointer
                            relative
                        "
                    >
                        <div class="bg-black h-full w-full"></div>

                        <img 
                            class="absolute z-20 pointer-events-none"
                            src="~/assets/images/mobile-case.png"
                        >

                        <img 
                            class="absolute right-4 bottom-6 z-20"
                            width="90"
                            src="~/assets/images/tiktok-logo-white.png"
                        >

                        <video
                            autoplay
                            loop
                            muted
                            class="absolite rounded-3xl object-cover z-10 w-full h-full"
                            src="/car.mp4" 
                        />

                        <div class="absolute -bottom-12 flex items-center justify-between z-50 rounded-xl border w-full p-2 border-gray-300">
                            <div class="flex items-center truncate">
                                <Icon name="clarity:success-standard-line" size="16" class="min-w-[16px]" />
                                <div class="text-[11px] pl-1 truncate text-ellipsis">video name</div>
                            </div>

                            <button class="text-[11px] ml-2 font-semibold">
                                Change
                            </button>
                        </div>
                    </div>

                    <div class="mt-4 mb-6">
                        <div class="flex bg-[#F8F8F8] py-4 px-6">
                            <div>
                                <Icon class="mr-4" size="20" name="mdi:box-cutter-off" />
                            </div>
                            <div>
                                <div class="text-semibold text-[15px] mb-1.5">Divide videos and edit</div>
                                <div class="text-semibold text-[13px] text-gray-400">
                                    You can quickly divide video into multiple parts, 
                                    remove redundant parts and turn landscape videos into portrait videos
                                </div>
                            </div>
                            <div class="flex justify-end max-w-[130px] w-full h-full text-center my-auto">
                                <button class="px-8 py-1.5 text-white text-[15px] bg-[#F02C56] rounded-sm">
                                    Edit
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </UploadLayout>
    </div>
</template>

<script setup>
    import UploadLayout from "~~/layouts/UploadLayout.vue";
</script>